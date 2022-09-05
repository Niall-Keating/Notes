# How Does Netflix Scale P...

![rw-book-cover](https://pbs.twimg.com/profile_images/1524184008635998209/vOSCJXuk.jpg)

## Metadata
- Author: [[@alexxubyte on Twitter]]
- Full Title: How Does Netflix Scale P...
- Category: #tweets
- URL: https://twitter.com/alexxubyte/status/1559929312828043265

## Highlights
- How does Netflix scale push messaging for millions of devices?
  This post draws from an article published on Netflix’s engineering blog. Here’s my understanding of how the online streaming giant’s system works. 
  ![](https://pbs.twimg.com/media/FaX7cIvVUAEhzMk.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1559929312828043265))
- 𝐑𝐞𝐪𝐮𝐢𝐫𝐞𝐦𝐞𝐧𝐭𝐬 & 𝐬𝐜𝐚𝐥𝐞
  - 220 million users
  - Near real-time
  - Backend systems need to send notifications to various clients
  - Supported clients: iOS, Android, smart TVs, Roku, Amazon FireStick, web browser ([View Tweet](https://twitter.com/alexxubyte/status/1559929316468613121))
- 𝐓𝐡𝐞 𝐥𝐢𝐟𝐞 𝐨𝐟 𝐚 𝐩𝐮𝐬𝐡 𝐧𝐨𝐭𝐢𝐟𝐢𝐜𝐚𝐭𝐢𝐨𝐧
  1. Push notification events are triggered by the clock, user actions, or by systems.
  2. Events are sent to the event management engine. 
  ![](https://pbs.twimg.com/media/FaX7czeVEAE9ub9.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1559929325322788864))
- 3. The event management engine listens to specific events and forward events to different queues. The queues are populated by priority-based event forwarding rules
  4. The “event priority-based processing cluster” processes events and generates push notifications data for devices 
  ![](https://pbs.twimg.com/media/FaX7dXCUsAAhTkU.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1559929335787573253))
- 5. A Cassandra database is used to store the notification data.
  6. A push notification is sent to outbound messaging systems. 
  ![](https://pbs.twimg.com/media/FaX7d94VsAEs7vE.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1559929345879052290))
- 7. For Android, FCM is used to send push notifications. For Apple devices, APNs are used. For web, TV, and other streaming devices, Netflix’s homegrown solution called ‘Zuul Push’ is used. 
  ![](https://pbs.twimg.com/media/FaX7ejoUcAA579Q.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1559929355869925376))
- Over to you: if you wanted to support every kind of device, which delivery model would work better, push or pull-based notifications? ([View Tweet](https://twitter.com/alexxubyte/status/1559929359909019648))
- Subscribe to our weekly newsletter to learn something new every week ⇩:
  https://t.co/PczMAd8Jdb
  #systemdesign #coding #interviewtips ([View Tweet](https://twitter.com/alexxubyte/status/1559929362324996096))
- Link: https://t.co/mPdxCVdhJE ([View Tweet](https://twitter.com/alexxubyte/status/1560040085080264704))
