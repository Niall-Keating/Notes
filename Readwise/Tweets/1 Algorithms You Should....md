# /1 Algorithms You Should...

![rw-book-cover](https://pbs.twimg.com/profile_images/1524184008635998209/vOSCJXuk.jpg)

## Metadata
- Author: [[@alexxubyte on Twitter]]
- Full Title: /1 Algorithms You Should...
- Category: #tweets
- URL: https://twitter.com/alexxubyte/status/1554851895826558976

## Highlights
- /1 Algorithms you should know series for System Design.
  𝐀𝐥𝐠𝐨𝐫𝐢𝐭𝐡𝐦 1: 𝐂𝐨𝐧𝐬𝐢𝐬𝐭𝐞𝐧𝐭 𝐇𝐚𝐬𝐡𝐢𝐧𝐠
  If you prefer video, you can watch our YouTube video here ⇩
  https://t.co/4fRz617p3u
  If you prefer text, keep reading: 
  ![](https://pbs.twimg.com/media/FZPxjppUsAIoVod.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1554851895826558976))
- /2 What do Amazon DynamoDB, Apache Cassandra, Discord, and Akamai CDN have in common?
  They all use consistent hashing. Let’s dive right in. ([View Tweet](https://twitter.com/alexxubyte/status/1554851899156733952))
- /3 𝐖𝐡𝐚𝐭’𝐬 𝐭𝐡𝐞 𝐢𝐬𝐬𝐮𝐞 𝐰𝐢𝐭𝐡 𝐬𝐢𝐦𝐩𝐥𝐞 𝐡𝐚𝐬𝐡𝐢𝐧𝐠?
  In a large-scale distributed system, data does not fit on a single server. They are “distributed” across many machines. This is called horizontal scaling. ([View Tweet](https://twitter.com/alexxubyte/status/1554851901841162241))
- /4 To build such a system with predictable performance, it is important to distribute the data evenly across those servers.
  Simple hashing: serverIndex = hash(key) % N, where N is the size of the server pool ([View Tweet](https://twitter.com/alexxubyte/status/1554851904399609858))
- /5 This approach works well when the size of the cluster is fixed, and the data distribution is even. But when new servers get added to meet new demand, or when existing servers get removed, it triggers a storm of misses and a lot of objects to be moved. ([View Tweet](https://twitter.com/alexxubyte/status/1554851906974994433))
- /6 𝐂𝐨𝐧𝐬𝐢𝐬𝐭𝐞𝐧𝐭 𝐡𝐚𝐬𝐡𝐢𝐧𝐠
  Consistent hashing is an effective technique to mitigate this issue.
  The goal of consistent hashing is simple. We want almost all objects to stay assigned to the same server even as the number of servers changes. 
  ![](https://pbs.twimg.com/media/FZPxkqQUsAEcxWw.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1554851915069943813))
- /7 As shown in the diagram, using a hash function, we hash each server by its name or IP address, and place the server onto the ring. Next, we hash each object by its key with the same hashing function. 
  ![](https://pbs.twimg.com/media/FZPxlKqUIAAAPdf.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1554851923152343041))
- /8 To locate the server for a particular object, we go clockwise from the location of the object key on the ring until a server is found. Continue with our example, key 0 is on server 0, key 1 is on server 1. 
  ![](https://pbs.twimg.com/media/FZPxlnzUEAAjtlK.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1554851930857299969))
- /9 𝐀𝐝𝐝 𝐚 𝐬𝐞𝐫𝐯𝐞𝐫
  Now let’s take a look at what happens when we add a server. ([View Tweet](https://twitter.com/alexxubyte/status/1554851934036627456))
- /10 Here we insert a new server s4 to the left of s0 on the ring. Note that only k0 needs to be moved from s0 to s4. This is because s4 is the first server k0 encounters by going clockwise from k0’s position on the ring. Keys k1, k2, and k3 are not affected. 
  ![](https://pbs.twimg.com/media/FZPxmOOUUAEBQku.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1554851941703774208))
- /11 𝐇𝐨𝐰 𝐜𝐨𝐧𝐬𝐢𝐬𝐭𝐞𝐧𝐭 𝐡𝐚𝐬𝐡𝐢𝐧𝐠 𝐢𝐬 𝐮𝐬𝐞𝐝 𝐢𝐧 𝐭𝐡𝐞 𝐫𝐞𝐚𝐥 𝐰𝐨𝐫𝐥𝐝
  🔹Amazon DynamoDB and Apache Cassandra: minimize data movement during rebalancing
  🔹Content delivery networks like Akamai: distribute web contents evenly among the edge servers ([View Tweet](https://twitter.com/alexxubyte/status/1554851944895692800))
- /12 🔹Load balancers like Google Network Load Balancer: distribute persistent connections evenly across backend servers
  Over to you - which algorithm should we talk about next? ([View Tweet](https://twitter.com/alexxubyte/status/1554851947441577984))
- /13 I hope you've found this thread helpful.
  Follow me @alexxubyte for more.
  Like/Retweet the first tweet below if you can: https://t.co/LXasnfljrD ([View Tweet](https://twitter.com/alexxubyte/status/1554851950012772352))
