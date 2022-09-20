# /1 Choosing the Right Da...

![rw-book-cover](https://pbs.twimg.com/profile_images/1524184008635998209/vOSCJXuk.jpg)

## Metadata
- Author: [[@alexxubyte on Twitter]]
- Full Title: /1 Choosing the Right Da...
- Category: #tweets
- URL: https://twitter.com/alexxubyte/status/1567901844994928641

## Highlights
- /1 Choosing the right database is often the most important decision we'll ever make.
  We are talking about a database for a real growing business, where a bad choice would lead to extended downtime, customer impact, and even data loss.
  This take is probably a bit controversial. 
  ![](https://pbs.twimg.com/media/FcJOaoPagAAg8rt.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1567901844994928641))
- /2 The thread was written by @sahnlam and illustrated by me. ([View Tweet](https://twitter.com/alexxubyte/status/1567901850271383552))
- /3 𝐅𝐢𝐫𝐬𝐭, 𝐚𝐫𝐞 𝐰𝐞 𝐩𝐨𝐬𝐢𝐭𝐢𝐯𝐞 𝐭𝐡𝐚𝐭 𝐰𝐞 𝐧𝐞𝐞𝐝 𝐚 𝐝𝐢𝐟𝐟𝐞𝐫𝐞𝐧𝐭 𝐝𝐚𝐭𝐚𝐛𝐚𝐬𝐞? Is the existing database breaking at the seams? Maybe the p95 latency is through the roof. Maybe the working set is overflowing the available memory. ([View Tweet](https://twitter.com/alexxubyte/status/1567901852938956800))
- /4 𝐖𝐡𝐚𝐭𝐞𝐯𝐞𝐫 𝐭𝐡𝐞 𝐢𝐬𝐬𝐮𝐞𝐬 𝐚𝐫𝐞, 𝐦𝐚𝐤𝐞 𝐬𝐮𝐫𝐞 𝐭𝐡𝐞𝐲 𝐚𝐫𝐞 𝐧𝐨𝐭 𝐞𝐚𝐬𝐢𝐥𝐲 𝐬𝐨𝐥𝐯𝐚𝐛𝐥𝐞.
  Let’s read the database manual of our current database system. There could be configuration knobs that we can tweak to give us a bit more breathing room. ([View Tweet](https://twitter.com/alexxubyte/status/1567901855614902274))
- /5 Can we put a cache in front of it, and give us a few more months of runway?
  Can we add read replicas to shed some read load?
  Can we shard the database, or partition the data in some way? ([View Tweet](https://twitter.com/alexxubyte/status/1567901858370551808))
- /6 The bottom line is this: Migrating live production data is risky and costly. We better be damn sure that there is no way to keep using the current database.
  We have exhausted all avenues for the current database. ([View Tweet](https://twitter.com/alexxubyte/status/1567901861054939136))
- /7 𝐇𝐨𝐰 𝐝𝐨 𝐰𝐞 𝐠𝐨 𝐚𝐛𝐨𝐮𝐭 𝐜𝐡𝐨𝐨𝐬𝐢𝐧𝐠 𝐭𝐡𝐞 𝐧𝐞𝐱𝐭 𝐨𝐧𝐞?
  We developers are naturally drawn to the new and shiny, like moths to flame. When it comes to databases, though, boring is good. ([View Tweet](https://twitter.com/alexxubyte/status/1567901863739281408))
- /8 We should prefer the ones that have been around for a long time, and have been battle tested. ([View Tweet](https://twitter.com/alexxubyte/status/1567901866473979904))
- /9 𝐒𝐨𝐟𝐭𝐰𝐚𝐫𝐞 𝐞𝐧𝐠𝐢𝐧𝐞𝐞𝐫𝐢𝐧𝐠 𝐚𝐭 𝐬𝐜𝐚𝐥𝐞 𝐢𝐬 𝐚𝐛𝐨𝐮𝐭 𝐭𝐫𝐚𝐝𝐞𝐨𝐟𝐟𝐬. 𝐖𝐡𝐞𝐧 𝐢𝐭 𝐜𝐨𝐦𝐞𝐬 𝐭𝐨 𝐝𝐚𝐭𝐚𝐛𝐚𝐬𝐞𝐬, 𝐢𝐭 𝐢𝐬 𝐞𝐯𝐞𝐧 𝐦𝐨𝐫𝐞 𝐭𝐫𝐮𝐞. ([View Tweet](https://twitter.com/alexxubyte/status/1567901869183479808))
- /10 Instead of reading the shiny brochures, go read the manual. There is usually a page called “Limits”. That page is a gem.
  Learn as much as possible about the candidate now. The investment is relatively small at this juncture. ([View Tweet](https://twitter.com/alexxubyte/status/1567901871947534338))
- /11 𝐎𝐧𝐜𝐞 𝐰𝐞 𝐧𝐚𝐫𝐫𝐨𝐰 𝐝𝐨𝐰𝐧 𝐭𝐡𝐞 𝐝𝐚𝐭𝐚𝐛𝐚𝐬𝐞 𝐨𝐩𝐭𝐢𝐨𝐧𝐬, 𝐰𝐡𝐚𝐭’𝐬 𝐧𝐞𝐱𝐭?
  Create a realistic test bench for the candidates using our data, with our real-world access patterns. ([View Tweet](https://twitter.com/alexxubyte/status/1567901874736758787))
- /12 During benchmarking, pay attention to the outliers. Measure P99 of everything. The average is not meaningful.
  After everything checks out, plan the migration carefully. Write out a detailed step-by-step migration plan. ([View Tweet](https://twitter.com/alexxubyte/status/1567901877484007430))
- /13 Picking the right database is not glamorous, and there is a lot of hard work involved. Migrating to a new database in the real world could take years at a high scale.
  Good luck. ([View Tweet](https://twitter.com/alexxubyte/status/1567901880130613248))
- /14 I hope you've found this thread helpful.
  Follow me @alexxubyte for more.
  Like/Retweet the first tweet below if you can: https://t.co/rn3ePtp31o ([View Tweet](https://twitter.com/alexxubyte/status/1567901882827554818))
