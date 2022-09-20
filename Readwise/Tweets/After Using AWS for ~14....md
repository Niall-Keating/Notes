# After Using AWS for ~14...

![rw-book-cover](https://pbs.twimg.com/profile_images/1199447204311617537/vzdPtfih.jpg)

## Metadata
- Author: [[@__steele on Twitter]]
- Full Title: After Using AWS for ~14...
- Category: #tweets
- URL: https://twitter.com/__steele/status/1570208081296134145

## Highlights
- After using AWS for ~14 years, I've internalised a handful of design patterns that I try to apply to my own software. I'm keen to know if it's the same for other folks.
  Roughly: tags, IDs (thrice), limits, pagination.
  (I'm not going to use the thread emoji) ([View Tweet](https://twitter.com/__steele/status/1570208081296134145))
- 1: Tags.
  A lot of software has support for tags, but it's usually a set of strings. This is useful in the case of "show me all resources tagged 'engineering'". Or even "show me all resources tagged 'engineering' and 'frontend'". ([View Tweet](https://twitter.com/__steele/status/1570208083154210816))
- AWS resources go one step further and implement key-value tags. So in addition to the above, you can ask the question "show me all resources grouped by the 'department' tag key". This is super useful for power users, folks in finance, etc. ([View Tweet](https://twitter.com/__steele/status/1570208085209391112))
- 2: Resource ID prefixes
  Almost all objects in a web service will have some kind of ID. It might be an auto-incrementing integer, or a GUID, a random string, etc. 
  When debugging, you will often ask a user for the ID of the misbehaving object. You look, but it's not in the DB?? ([View Tweet](https://twitter.com/__steele/status/1570208087134605312))
- Turns out they gave you a session ID instead of an order ID. Doh!
  This is where resource ID *prefixes* are insanely useful. Think EC2 instance IDs: i-abc123 or EBS volumes: vol-def456.
  Now when you ask a user for an ID, you'll know immediately if it's the wrong thing entirely. ([View Tweet](https://twitter.com/__steele/status/1570208088988483586))
- 2b: Fully qualified IDs
  Sometimes an object ID by itself isn't enough. You store your data hierarchically on S3, so an invoice ID alone can't find its PDF. You also need the customer ID. 
  This is where AWS uses ARNs. An ARN should be sufficient to locate the stored object. ([View Tweet](https://twitter.com/__steele/status/1570208090750087168))
- E.g. instead of passing around invoice IDs like inv-12345, you pass fully qualified IDs like eu:c-acd223:inv-12345. With that string, your code knows the PDF is in the EU partition, under the c-acd223 customer directory, file name inv-12345.pdf. Much quicker troubleshooting. ([View Tweet](https://twitter.com/__steele/status/1570208092398424064))
- AWS doesn't always get this right! When ECS first launched, task ARNs were of the format arn:aws:ecs:${region}:${account}:task/${taskId}. But you could have multiple clusters in a single region - so which cluster do you look up?
  They later migrated to :task/${cluster}/${taskId}. ([View Tweet](https://twitter.com/__steele/status/1570208094080348160))
- 2c: ULIDs > GUIDs >> Integers
  This is a bonus one on the theme of IDs, because I don't think AWS does it.
  GUIDs are better than auto-incrementing integer IDs because they don't reveal the number of objects in your DB and they don't have contention on the "next ID" counter. ([View Tweet](https://twitter.com/__steele/status/1570208095875497986))
- But ULIDs are better than GUIDs because they encode creation timestamps in the prefix. This means they are naturally sortable by creation time. This is useful for databases like DynamoDB or Redshift where data can be stored sorted and you can easily return the latest N objects. ([View Tweet](https://twitter.com/__steele/status/1570208097607745536))
- It's also useful in unexpected places. Maybe you think you don't need creation timestamp in your customer IDs? I mean, how often are they created? And they rarely ever need to be sorted. ([View Tweet](https://twitter.com/__steele/status/1570208099306442752))
- What about when you migrate data store? Your proxy (in the hot path of every request) can forward any customers created after date X to service B and older ones to service A -- all without needing a roundtrip to the DB to look up if they were created before/after the cutover. ([View Tweet](https://twitter.com/__steele/status/1570208101130997762))
- 3: Limits.
  AWS publishes limits for just about every service. This serves a number of purposes. 
  * They can build a service with reliable performance because they know there will never be 10,000x more objects than anticipated during system design. ([View Tweet](https://twitter.com/__steele/status/1570208102821273602))
- * Customers can be confident that the service can handle their use case, because it's well within the published limits. Their app isn't going to break because it will hit a pathological behaviour in the AWS service. ([View Tweet](https://twitter.com/__steele/status/1570208104545161216))
- * Limits can always be raised over time, or in response to a customer request. This means AWS can provision an appropriate level of resourcing.
  IMO, limits show a level of professionalism. It means that the service operator understands what their service can -- and cannot -- do. ([View Tweet](https://twitter.com/__steele/status/1570208106117988354))
- 4: Pagination.
  Every AWS service (that I can think of) uses "next page" cursors for pagination, not page indexes. Hell, maybe they *do* use page indexes under the hood, but that is an *implementation detail* that is not exposed in the opaque "next page" cursor. ([View Tweet](https://twitter.com/__steele/status/1570208107925766144))
- This gives you the ability to implement pagination with ease. If your data store is DynamoDB, you can return a wrapped DynamoDB pagination token to your users. ([View Tweet](https://twitter.com/__steele/status/1570208109670572032))
- You can also migrate data stores. Maybe you're moving from one that supports page indexes to one that doesn't. Now you don't need to break your API contract or introduce a new v2 API with different pagination. ([View Tweet](https://twitter.com/__steele/status/1570208111826436102))
- Maybe your pages need an expensive query to a SQL DB. You don't want to have to repeat that query 10x for 10 pages and throw away 90% of the data each time. This makes your DBA sad. ([View Tweet](https://twitter.com/__steele/status/1570208113533550593))
- Instead, on page 1 you retrieve the whole dataset and store it in Redis under a GUID. Now your pagination token can be that GUID + an offset into the Redis array. Now your pages are super speedy to load. You have a happy DBA. ([View Tweet](https://twitter.com/__steele/status/1570208115441934337))
- Also on pagination: your docs should make explicit that the number of results on a page can be ≤ ${pageSize}. 
  This means that you can have more predictable performance for your API. You can make sure a page is never more than 1MB of data. ([View Tweet](https://twitter.com/__steele/status/1570208117094481920))
- Or that a page doesn't spill over to a second DB partition and take 15x longer to load as the previous page. ([View Tweet](https://twitter.com/__steele/status/1570208118789001216))
- PS: don't forget to encrypt your pagination token, or users will reverse engineer the format and start crafting their own. Ideally using AEAD, so they can't tamper with it at all - and the encryption context should include the customer ID to avoid data leaks. ([View Tweet](https://twitter.com/__steele/status/1570208120860995584))
- Anyway, that's all I can think of for now. Do you have any others that I missed?
  I partially wrote this list for that sweet Twitter fame, but mostly so I have a reference for when my colleague @kmcquade3 asks why I'm implementing something a particular way. ([View Tweet](https://twitter.com/__steele/status/1570208122832326657))
- Daniel had a really good bonus one: Access key IDs. 
  By having long-lived access key IDs in a regex-able format (e.g AKIA[XX…]) it allows you to detect secret leaks. 
  GitHub even lets software vendors register their credential regexes and get webhooks on leaks == auto-revoke https://t.co/XBIzTzIdNl ([View Tweet](https://twitter.com/__steele/status/1570321500699529217))
