# /1 How Do Big Keys Impac...

![rw-book-cover](https://pbs.twimg.com/profile_images/1524184008635998209/vOSCJXuk.jpg)

## Metadata
- Author: [[@alexxubyte on Twitter]]
- Full Title: /1 How Do Big Keys Impac...
- Category: #tweets
- URL: https://twitter.com/alexxubyte/status/1571880260177907713

## Highlights
- /1 How do big keys impact Redis persistence? We call a key that contains a large size of data a big key. For example, the size of the key is 5 MB.
  The diagram shows how big keys impact Redis AOF (Append-Only-File) persistence. 
  ![](https://pbs.twimg.com/media/FdBww15aEAQHxdd.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1571880260177907713))
- /2 There are three modes when we turn on AOF persistence:
  1️⃣ Always - synchronously write data to the disk whenever there is a data update in memory.
  2️⃣ EverySec - write to the disk every second. ([View Tweet](https://twitter.com/alexxubyte/status/1571880263818555394))
- /3 3️⃣ No - Redis doesn’t control when the data is written to the dis. Instead, the operating system decides when the data is written to the disk.
  👉 How do we analyze the impact of big keys? ([View Tweet](https://twitter.com/alexxubyte/status/1571880266511294464))
- /4 Redis writes keys into memory first, then calls write() to write the data into the kernel buffer cache. Then fsync() flushes all modified in-core data of the file to the disk device There are 3 modes. ([View Tweet](https://twitter.com/alexxubyte/status/1571880269283758080))
- /5 In “Always” mode, it calls fsync() synchronously. If we need to update a big key, the main thread will be blocked because it has to wait for the write to complete. 
  ![](https://pbs.twimg.com/media/FdBwxzuaMAE_aeD.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1571880278129508352))
- /6 “EveySec” starts a background timer task to call fsync() every second, so big keys have no impact on the Redis main thread. 
  ![](https://pbs.twimg.com/media/FdBwyWdacAMiKI-.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1571880288472694784))
- /7 “No” mode never calls fsync(). It is up to the operating system. Big keys have no impact on the main thread. 
  ![](https://pbs.twimg.com/media/FdBwy-daIAAHPYs.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1571880298887122944))
- /8 Over to you: How to avoid big keys? ([View Tweet](https://twitter.com/alexxubyte/status/1571880302578110470))
