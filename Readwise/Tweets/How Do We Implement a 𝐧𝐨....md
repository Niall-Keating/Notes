# How Do We Implement a π§π¨...

![rw-book-cover](https://pbs.twimg.com/profile_images/1524184008635998209/vOSCJXuk.jpg)

## Metadata
- Author: [[@alexxubyte on Twitter]]
- Full Title: How Do We Implement a π§π¨...
- Category: #tweets
- URL: https://twitter.com/alexxubyte/status/1542882527110541312

## Highlights
- How do we implement a π§π¨π§-ππ₯π¨ππ€π’π§π  queue? What are the differences between blocking and non-blocking algorithms? 
  ![](https://pbs.twimg.com/media/FWlrep4VQAAz-N-.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1542882527110541312))
- The terms we use when discussing blocking and non-blocking algorithms can be confusing, so letβs start by reviewing the terminology in the concurrency area with a diagram. 
  ![](https://pbs.twimg.com/media/FWlrfKxVsAAHyjc.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1542882537231462401))
- πΉblocking
  The blocking algorithm uses locks. Thread A acquires the lock first, and Thread B might wait for arbitrary lengthy periods if Thread A gets suspended while holding the lock. This algorithm may cause Thread B to starve. 
  ![](https://pbs.twimg.com/media/FWlrfu2UIAIjYkw.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1542882547608141824))
- πΉnon-blocking:
  The non-blocking algorithm allows Thread A to access the queue, but Thread A must complete a task in a certain number of steps. Other threads like Thread B may still starve due to the rejections. 
  ![](https://pbs.twimg.com/media/FWlrgWTUUAEZaIG.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1542882557913575424))
- This is the main ππ’ππππ«ππ§ππ between blocking and non-blocking algorithms: The blocking algorithm blocks Thread B until the lock is released. A non-blocking algorithm notifies Thread B that access is rejected. 
  ![](https://pbs.twimg.com/media/FWlrg8qUYAcn9nX.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1542882568286089216))
- πΉstarvation-free:
  Thread Starvation means a thread cannot acquire access to certain shared resources and cannot proceed. Starvation-free means this situation does not occur.
  πΉwait-free:
  All threads can complete the tasks within a finite number of steps. ([View Tweet](https://twitter.com/alexxubyte/status/1542882572459421698))
- ππ’πͺπ΅-π§π³π¦π¦ = ππ°π―-ππ­π°π€π¬πͺπ―π¨ + ππ΅π’π³π·π’π΅πͺπ°π―-π§π³π¦π¦
  β‘οΈ Non-Blocking Queue ππ¦π©π₯ππ¦ππ§π­ππ­π’π¨π§
  We can use Compare and Swap (CAS) to implement a non-blocking queue. The diagram below illustrates the algorithm. 
  ![](https://pbs.twimg.com/media/FWlrhsaVEAECCvf.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1542882580973834241))
- β‘οΈ πππ§πππ’π­π¬
  1. No thread suspension. Thread B can get a response immediately and then decide what to do next. In this way, the thread latency is greatly reduced. ([View Tweet](https://twitter.com/alexxubyte/status/1542882585386180610))
- 2. No deadlocks. Threads A and B do not wait for the lock to release, meaning that there is no possibility of a deadlock occurring. ([View Tweet](https://twitter.com/alexxubyte/status/1542882587995123712))
- Subscribe to my weekly newsletter to learn something new every week: https://t.co/0RYwcKv26q ([View Tweet](https://twitter.com/alexxubyte/status/1542882590541066240))
