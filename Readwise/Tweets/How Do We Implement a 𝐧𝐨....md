# How Do We Implement a 𝐧𝐨...

![rw-book-cover](https://pbs.twimg.com/profile_images/1524184008635998209/vOSCJXuk.jpg)

## Metadata
- Author: [[@alexxubyte on Twitter]]
- Full Title: How Do We Implement a 𝐧𝐨...
- Category: #tweets
- URL: https://twitter.com/alexxubyte/status/1542882527110541312

## Highlights
- How do we implement a 𝐧𝐨𝐧-𝐛𝐥𝐨𝐜𝐤𝐢𝐧𝐠 queue? What are the differences between blocking and non-blocking algorithms? 
  ![](https://pbs.twimg.com/media/FWlrep4VQAAz-N-.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1542882527110541312))
- The terms we use when discussing blocking and non-blocking algorithms can be confusing, so let’s start by reviewing the terminology in the concurrency area with a diagram. 
  ![](https://pbs.twimg.com/media/FWlrfKxVsAAHyjc.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1542882537231462401))
- 🔹blocking
  The blocking algorithm uses locks. Thread A acquires the lock first, and Thread B might wait for arbitrary lengthy periods if Thread A gets suspended while holding the lock. This algorithm may cause Thread B to starve. 
  ![](https://pbs.twimg.com/media/FWlrfu2UIAIjYkw.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1542882547608141824))
- 🔹non-blocking:
  The non-blocking algorithm allows Thread A to access the queue, but Thread A must complete a task in a certain number of steps. Other threads like Thread B may still starve due to the rejections. 
  ![](https://pbs.twimg.com/media/FWlrgWTUUAEZaIG.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1542882557913575424))
- This is the main 𝐝𝐢𝐟𝐟𝐞𝐫𝐞𝐧𝐜𝐞 between blocking and non-blocking algorithms: The blocking algorithm blocks Thread B until the lock is released. A non-blocking algorithm notifies Thread B that access is rejected. 
  ![](https://pbs.twimg.com/media/FWlrg8qUYAcn9nX.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1542882568286089216))
- 🔹starvation-free:
  Thread Starvation means a thread cannot acquire access to certain shared resources and cannot proceed. Starvation-free means this situation does not occur.
  🔹wait-free:
  All threads can complete the tasks within a finite number of steps. ([View Tweet](https://twitter.com/alexxubyte/status/1542882572459421698))
- 𝘞𝘢𝘪𝘵-𝘧𝘳𝘦𝘦 = 𝘕𝘰𝘯-𝘉𝘭𝘰𝘤𝘬𝘪𝘯𝘨 + 𝘚𝘵𝘢𝘳𝘷𝘢𝘵𝘪𝘰𝘯-𝘧𝘳𝘦𝘦
  ➡️ Non-Blocking Queue 𝐈𝐦𝐩𝐥𝐞𝐦𝐞𝐧𝐭𝐚𝐭𝐢𝐨𝐧
  We can use Compare and Swap (CAS) to implement a non-blocking queue. The diagram below illustrates the algorithm. 
  ![](https://pbs.twimg.com/media/FWlrhsaVEAECCvf.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1542882580973834241))
- ➡️ 𝐁𝐞𝐧𝐞𝐟𝐢𝐭𝐬
  1. No thread suspension. Thread B can get a response immediately and then decide what to do next. In this way, the thread latency is greatly reduced. ([View Tweet](https://twitter.com/alexxubyte/status/1542882585386180610))
- 2. No deadlocks. Threads A and B do not wait for the lock to release, meaning that there is no possibility of a deadlock occurring. ([View Tweet](https://twitter.com/alexxubyte/status/1542882587995123712))
- Subscribe to my weekly newsletter to learn something new every week: https://t.co/0RYwcKv26q ([View Tweet](https://twitter.com/alexxubyte/status/1542882590541066240))
