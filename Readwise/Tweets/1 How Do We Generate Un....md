# /1 How Do We Generate Un...

![rw-book-cover](https://pbs.twimg.com/profile_images/1524184008635998209/vOSCJXuk.jpg)

## Metadata
- Author: [[@alexxubyte on Twitter]]
- Full Title: /1 How Do We Generate Un...
- Category: #tweets
- URL: https://twitter.com/alexxubyte/status/1570430639836639239

## Highlights
- /1 How do we generate unique IDs in distributed systems? How do we avoid ID conflicts?
  The diagram below shows 5 ways. 👇 
  ![](https://pbs.twimg.com/media/FctKVyQaIAINUk2.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1570430639836639239))
- /2 Assume the design requirements of distributed unique ID are:
  1. Globally unique.
  2. Availability. The ID generator must be available under high concurrency.
  3. Ordered. The IDs are sorted by certain rules. For example, sorted by time. ([View Tweet](https://twitter.com/alexxubyte/status/1570430644639137792))
- /3 4. Distributed. The ID generator doesn’t rely on a centralized service.
  5. Security. Depending on the use case, some IDs cannot be incremental integers, which might expose sensitive info. For example, people might guess the total user number correctly by looking at the IDs. ([View Tweet](https://twitter.com/alexxubyte/status/1570430647281537024))
- /4 Over to you: 1) Could you think of any use cases that unique IDs are useful?
  2）There are variations in the snowflake implementation. For example, data center ID can be added to the “MachineID” section to guarantee global uniqueness. Do you know other variations? ([View Tweet](https://twitter.com/alexxubyte/status/1570430649953296387))
- /5 I hope you've found this thread helpful.
  - Like/Retweet the first tweet below if you can.
  - Follow me @alexxubyte for more.
  - I write about system design and book writing tips. https://t.co/rAbhizkYWk ([View Tweet](https://twitter.com/alexxubyte/status/1570430652679614465))
