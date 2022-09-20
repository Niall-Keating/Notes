# /1 What Does API Gateway...

![rw-book-cover](https://pbs.twimg.com/profile_images/1524184008635998209/vOSCJXuk.jpg)

## Metadata
- Author: [[@alexxubyte on Twitter]]
- Full Title: /1 What Does API Gateway...
- Category: #tweets
- URL: https://twitter.com/alexxubyte/status/1567177071725793283

## Highlights
- /1 What does API gateway do?
  The diagram below shows the detail. 
  ![](https://pbs.twimg.com/media/Fb-7PINaMAMwGse.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1567177071725793283))
- /2 Step 1 - The client sends an HTTP request to the API gateway.
  Step 2 - The API gateway parses and validates the attributes in the HTTP request.
  Step 3 - The API gateway performs whitelist or blacklist checks. 
  ![](https://pbs.twimg.com/media/Fb-7Px5aQAMAyQH.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1567177082551271432))
- /3 Step 4 - The API gateway talks to an identity provider for authentication and authorization.
  Step 5 - The rate limiting rules are applied to the request. If it is over the limit, the request is rejected. 
  ![](https://pbs.twimg.com/media/Fb-7QZmaQAASJhW.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1567177095281004545))
- /4 Steps 6 and 7 - Now that the request has passed basic checks, the API gateway finds the relevant service to route to by path matching.
  Step 8 - The API gateway transforms the request into the appropriate protocol and sends it to backend microservices. 
  ![](https://pbs.twimg.com/media/Fb-7RIPaMAAnQlL.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1567177106941186049))
- /5 Steps 9-12: The API gateway can handle errors properly, and deals with faults if the error takes a longer time to recover (circuit break). It can also leverage ELK (Elastic-Logstash-Kibana) stack for logging and monitoring. We sometimes cache data in the API gateway. 
  ![](https://pbs.twimg.com/media/Fb-7Rz3aUAAIRxy.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1567177118936887297))
- /6 Over to you: 1) What’s the difference between a load balancer and an API gateway?
  2) Do we need to use different API gateways for PC, mobile and browser separately? ([View Tweet](https://twitter.com/alexxubyte/status/1567177123001147394))
- /7 I hope you've found this thread helpful.
  Follow me @alexxubyte for more.
  Like/Retweet the first tweet below if you can: https://t.co/jCWNDbwzxj ([View Tweet](https://twitter.com/alexxubyte/status/1567177125744230402))
- Edit: update whitelist/blacklist to the modern equivalents allow-list/deny-list 
  ![](https://pbs.twimg.com/media/Fb_Lwc5aMAEn8VY.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1567195582565089286))
