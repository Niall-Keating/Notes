# /1 Algorithms You Should...

![rw-book-cover](https://pbs.twimg.com/profile_images/1524184008635998209/vOSCJXuk.jpg)

## Metadata
- Author: [[@alexxubyte on Twitter]]
- Full Title: /1 Algorithms You Should...
- Category: #tweets
- URL: https://twitter.com/alexxubyte/status/1554851895826558976

## Highlights
- /1 Algorithms you should know series for System Design.
  ๐๐ฅ๐ ๐จ๐ซ๐ข๐ญ๐ก๐ฆ 1: ๐๐จ๐ง๐ฌ๐ข๐ฌ๐ญ๐๐ง๐ญ ๐๐๐ฌ๐ก๐ข๐ง๐ 
  If you prefer video, you can watch our YouTube video here โฉ
  https://t.co/4fRz617p3u
  If you prefer text, keep reading: 
  ![](https://pbs.twimg.com/media/FZPxjppUsAIoVod.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1554851895826558976))
- /2 What do Amazon DynamoDB, Apache Cassandra, Discord, and Akamai CDN have in common?
  They all use consistent hashing. Letโs dive right in. ([View Tweet](https://twitter.com/alexxubyte/status/1554851899156733952))
- /3 ๐๐ก๐๐ญโ๐ฌ ๐ญ๐ก๐ ๐ข๐ฌ๐ฌ๐ฎ๐ ๐ฐ๐ข๐ญ๐ก ๐ฌ๐ข๐ฆ๐ฉ๐ฅ๐ ๐ก๐๐ฌ๐ก๐ข๐ง๐ ?
  In a large-scale distributed system, data does not fit on a single server. They are โdistributedโ across many machines. This is called horizontal scaling. ([View Tweet](https://twitter.com/alexxubyte/status/1554851901841162241))
- /4 To build such a system with predictable performance, it is important to distribute the data evenly across those servers.
  Simple hashing: serverIndex = hash(key) % N, where N is the size of the server pool ([View Tweet](https://twitter.com/alexxubyte/status/1554851904399609858))
- /5 This approach works well when the size of the cluster is fixed, and the data distribution is even. But when new servers get added to meet new demand, or when existing servers get removed, it triggers a storm of misses and a lot of objects to be moved. ([View Tweet](https://twitter.com/alexxubyte/status/1554851906974994433))
- /6 ๐๐จ๐ง๐ฌ๐ข๐ฌ๐ญ๐๐ง๐ญ ๐ก๐๐ฌ๐ก๐ข๐ง๐ 
  Consistent hashing is an effective technique to mitigate this issue.
  The goal of consistent hashing is simple. We want almost all objects to stay assigned to the same server even as the number of servers changes. 
  ![](https://pbs.twimg.com/media/FZPxkqQUsAEcxWw.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1554851915069943813))
- /7 As shown in the diagram, using a hash function, we hash each server by its name or IP address, and place the server onto the ring. Next, we hash each object by its key with the same hashing function. 
  ![](https://pbs.twimg.com/media/FZPxlKqUIAAAPdf.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1554851923152343041))
- /8 To locate the server for a particular object, we go clockwise from the location of the object key on the ring until a server is found. Continue with our example, key 0 is on server 0, key 1 is on server 1. 
  ![](https://pbs.twimg.com/media/FZPxlnzUEAAjtlK.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1554851930857299969))
- /9 ๐๐๐ ๐ ๐ฌ๐๐ซ๐ฏ๐๐ซ
  Now letโs take a look at what happens when we add a server. ([View Tweet](https://twitter.com/alexxubyte/status/1554851934036627456))
- /10 Here we insert a new server s4 to the left of s0 on the ring. Note that only k0 needs to be moved from s0 to s4. This is because s4 is the first server k0 encounters by going clockwise from k0โs position on the ring. Keys k1, k2, and k3 are not affected. 
  ![](https://pbs.twimg.com/media/FZPxmOOUUAEBQku.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1554851941703774208))
- /11 ๐๐จ๐ฐ ๐๐จ๐ง๐ฌ๐ข๐ฌ๐ญ๐๐ง๐ญ ๐ก๐๐ฌ๐ก๐ข๐ง๐  ๐ข๐ฌ ๐ฎ๐ฌ๐๐ ๐ข๐ง ๐ญ๐ก๐ ๐ซ๐๐๐ฅ ๐ฐ๐จ๐ซ๐ฅ๐
  ๐นAmazon DynamoDB and Apache Cassandra: minimize data movement during rebalancing
  ๐นContent delivery networks like Akamai: distribute web contents evenly among the edge servers ([View Tweet](https://twitter.com/alexxubyte/status/1554851944895692800))
- /12 ๐นLoad balancers like Google Network Load Balancer: distribute persistent connections evenly across backend servers
  Over to you - which algorithm should we talk about next? ([View Tweet](https://twitter.com/alexxubyte/status/1554851947441577984))
- /13 I hope you've found this thread helpful.
  Follow me @alexxubyte for more.
  Like/Retweet the first tweet below if you can: https://t.co/LXasnfljrD ([View Tweet](https://twitter.com/alexxubyte/status/1554851950012772352))
