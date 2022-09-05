# /1 Big Accounts, Such As...

![rw-book-cover](https://pbs.twimg.com/profile_images/1524184008635998209/vOSCJXuk.jpg)

## Metadata
- Author: [[@alexxubyte on Twitter]]
- Full Title: /1 Big Accounts, Such As...
- Category: #tweets
- URL: https://twitter.com/alexxubyte/status/1564279740390772736

## Highlights
- /1 Big accounts, such as Nike, Procter & Gamble & Nintendo, often cause hotspot issues for the payment system.
  A hotspot payment account is an account that has a large number of concurrent operations on it. 
  ![](https://pbs.twimg.com/media/FbVwIUMXEAAmdbH.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1564279740390772736))
- /2 For example, when merchant A starts a promotion on Amazon Prime day, it receives many concurrent purchasing orders. In this case, the merchant’s account in the database becomes a hotspot account due to frequent updates. ([View Tweet](https://twitter.com/alexxubyte/status/1564279744413110272))
- /3 In normal operations, we put a row lock on the merchant’s balance when it gets updated. However, this locking mechanism leads to low throughput and becomes a system bottleneck.
  The diagram below shows several optimizations. ([View Tweet](https://twitter.com/alexxubyte/status/1564279746946428928))
- /4 🔹Rate limit
  We can limit the number of requests within a certain period. The remaining requests will be rejected or retried at a later time. It is a simple way to increase the system’s responsiveness for some users, but this can lead to a bad user experience. 
  ![](https://pbs.twimg.com/media/FbVwJLpVQAAF4q7.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1564279758875025408))
- /5 🔹Split the balance account into sub-accounts
  We can set up sub-accounts for the merchant’s account. In this way, one update request only locks one sub-account, and the rest sub-accounts are still available. 
  ![](https://pbs.twimg.com/media/FbVwJ9SaAAAzc99.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1564279774746275840))
- /6 🔹Use cache to update balance first
  We can set up a caching layer to update the merchant’s balance. The detailed statements and balances are updated in the database later asynchronously. The in-memory cache can deal with much higher throughput than the database. 
  ![](https://pbs.twimg.com/media/FbVwK3SUYAA0Ou_.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1564279785999593472))
- /7 Over to you: We can also put the requests into a message queue so the requests can be processed at the service’s own pace. Can you think of the limitations of this approach? ([View Tweet](https://twitter.com/alexxubyte/status/1564279790143561728))
- /8 I hope you've found this thread helpful.
  Follow me @alexxubyte for more.
  Like/Retweet the first tweet below if you can: https://t.co/XPlo3l2oXE ([View Tweet](https://twitter.com/alexxubyte/status/1564279792651812864))
