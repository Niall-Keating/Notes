# We Just Published a YouT...

![rw-book-cover](https://pbs.twimg.com/profile_images/1524184008635998209/vOSCJXuk.jpg)

## Metadata
- Author: [[@alexxubyte on Twitter]]
- Full Title: We Just Published a YouT...
- Category: #tweets
- URL: https://twitter.com/alexxubyte/status/1542171218442211328

## Highlights
- We just published a YouTube video that explains why is Kafka fast.
  If you prefer video format, consider subscribing to our ByteByteGo youtube channel: 
  https://t.co/Abm5CkdvPE
  If you prefer text, you can keep reading: 
  ![](https://pbs.twimg.com/media/FWbkjDeUEAEpLUQ.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1542171218442211328))
- There are many design decisions that contributed to Kafka’s performance. In this post, we’ll focus on two. We think these two carried the most weight. ([View Tweet](https://twitter.com/alexxubyte/status/1542171222682656768))
- 1️⃣ Reliance on Sequential I/O.
  2️⃣ Focus on efficiency: zero copy principle.
  The diagram below illustrates how the data is transmitted between producer and consumer, and what zero-copy means. ([View Tweet](https://twitter.com/alexxubyte/status/1542171225236963328))
- 🔹Step 1.1 - 1.3: Producer writes data to the disk
  🔹Step 2: Consumer reads data without zero-copy
  2.1: The data is loaded from disk to OS cache
  2.2 The data is copied from OS cache to Kafka application
  2.3 Kafka application copies the data into the socket buffer 
  ![](https://pbs.twimg.com/media/FWbkj1rUIAA_rKV.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1542171233277489154))
- 2.4 The data is copied from socket buffer to network card
  2.5 The network card sends data out to the consumer
  🔹Step 3: Consumer reads data with zero-copy
  3.1: The data is loaded from disk to OS cache
  3.2 OS cache directly copies the data to the network card via sendfile() 
  ![](https://pbs.twimg.com/media/FWbkkY0UEAE_pB_.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1542171242786017282))
- 3.3 The network card sends data out to the consumer
  Zero copy is a shortcut to save the multiple data copies between application context and kernel context.
  Over to you: what are some of the other systems that rely on Sequential I/O? 
  ![](https://pbs.twimg.com/media/FWbkk7pVEAAK4oW.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1542171252315410433))
- Subscribe to our system design newsletter and YouTube channel to learn something new every week.
  𝐖𝐞𝐞𝐤𝐥𝐲 𝐧𝐞𝐰𝐬𝐥𝐞𝐭𝐭𝐞𝐫: https://t.co/dkjDPxrTOt
  𝐘𝐨𝐮𝐓𝐮𝐛𝐞 𝐜𝐡𝐚𝐧𝐧𝐞𝐥: https://t.co/erhdayLMag 
  ![](https://pbs.twimg.com/media/FWbklf1VEAEOCEr.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1542171260955676674))
