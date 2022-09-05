# /1 Is HTTPS Reliable?
I...

![rw-book-cover](https://pbs.twimg.com/profile_images/1524184008635998209/vOSCJXuk.jpg)

## Metadata
- Author: [[@alexxubyte on Twitter]]
- Full Title: /1 Is HTTPS Reliable?
I...
- Category: #tweets
- URL: https://twitter.com/alexxubyte/status/1562103641057607685

## Highlights
- /1 Is HTTPS reliable?
  If HTTPS is safe, how can tools like Fiddler capture network packets sent via HTTPS?
  The diagram below shows a scenario where a malicious intermediate hijacks the packets. 
  ![](https://pbs.twimg.com/media/Fa20-tQVQAkQMtG.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1562103641057607685))
- /2 Step 1 - The client requests to establish a TCP connection with the server. The request is maliciously routed to an intermediate server, instead of the real backend server. Then, a TCP connection is established between the client and the intermediate server. 
  ![](https://pbs.twimg.com/media/Fa20_NpVQAAI8rM.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1562103650511507456))
- /3 Step 2 - The intermediate server establishes a TCP connection with the actual server.
  Step 3 - The intermediate server sends the SSL certificate to the client. The certificate contains the public key, hostname, expiry dates, etc. The client validates the certificate. 
  ![](https://pbs.twimg.com/media/Fa20_wEUIAAC2Ee.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1562103658812059649))
- /4 Step 4 - The legitimate server sends its certificate to the intermediate server. The intermediate server validates the certificate. 
  ![](https://pbs.twimg.com/media/Fa21APnVsAMToYk.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1562103667364225024))
- /5 Step 5 - The client generates a session key and encrypts it using the public key from the intermediate server. The intermediate server receives the encrypted session key and decrypts it with the private key. 
  ![](https://pbs.twimg.com/media/Fa21AvUVQAEcehM.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1562103676218404866))
- /6 Step 6 - The intermediate server encrypts the session key using the public key from the actual server and then sends it there. The legitimate server decrypts the session key with the private key. 
  ![](https://pbs.twimg.com/media/Fa21BQdUIAAIwE1.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1562103685571702784))
- /7 Steps 7 and 8 - Now, the client and the server can communicate using the session key (symmetric encryption.) The encrypted data is transmitted in a secure bi-directional channel. The intermediate server can always decrypt the data. 
  ![](https://pbs.twimg.com/media/Fa21BzUUsAAS0M4.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1562103694425874434))
- /8 Now let’s answer the questions we started with:
  1. HTTPS is reliable, but the client should not accept a malicious certificate from an untrusted third-party server.
  2. Fiddler can decrypt the data because its certificate is accepted and trusted by the browser. ([View Tweet](https://twitter.com/alexxubyte/status/1562103698796425217))
- /9 Over to you: why does HTTPS use symmetric encryption for data transmission? Is it safe? ([View Tweet](https://twitter.com/alexxubyte/status/1562103701447196672))
- /10 I hope you've found this thread helpful.
  Follow me @alexxubyte for more.
  Like/Retweet the first tweet below if you can: https://t.co/5x747EWCus ([View Tweet](https://twitter.com/alexxubyte/status/1562103703997255680))
- Update to this thread.
  Prerequisite: root certificate of the intermediate server is present in the local trust-store. ([View Tweet](https://twitter.com/alexxubyte/status/1562247891451666432))
