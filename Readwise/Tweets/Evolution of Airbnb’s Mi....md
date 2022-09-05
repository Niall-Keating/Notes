# Evolution of Airbnb’s Mi...

![rw-book-cover](https://pbs.twimg.com/profile_images/1524184008635998209/vOSCJXuk.jpg)

## Metadata
- Author: [[@alexxubyte on Twitter]]
- Full Title: Evolution of Airbnb’s Mi...
- Category: #tweets
- URL: https://twitter.com/alexxubyte/status/1554494678937915394

## Highlights
- Evolution of Airbnb’s microservice architecture.
  This post is based on a tech talk. Check out the reference link at the end of the thread to read more.
  Help me reach 100k this week (System Design Newsletter currently at 97,160).
  Subscribe here: https://t.co/dkjDPxrTOt 
  ![](https://pbs.twimg.com/media/FZKsqw6UsAEjqeq.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1554494678937915394))
- 𝐌𝐨𝐧𝐨𝐥𝐢𝐭𝐡 (2008 - 2017)
  Airbnb began as a simple marketplace for hosts and guests. This is built in a Ruby on Rails application - the monolith.
  What’s the challenge?
  - Confusing team ownership + unowned code
  - Slow deployment 
  ![](https://pbs.twimg.com/media/FZKsrX2VsAA5PQC.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1554494690925326336))
- 𝐌𝐢𝐜𝐫𝐨𝐬𝐞𝐫𝐯𝐢𝐜𝐞𝐬 (2017 - 2020)
  Microservice aims to solve those challenges. In this architecture, key services include:
  - Data fetching service
  - Business logic data service
  - Write workflow service
  - UI aggregation service
  - Each service had one owning team 
  ![](https://pbs.twimg.com/media/FZKssFoVUAAZV-R.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1554494704191807489))
- What’s the challenge?
  Hundreds of services and dependencies were difficult for humans to manage. ([View Tweet](https://twitter.com/alexxubyte/status/1554494708730105856))
- 𝐌𝐢𝐜𝐫𝐨 + 𝐦𝐚𝐜𝐫𝐨𝐬𝐞𝐫𝐯𝐢𝐜𝐞𝐬 (2020 - present)
  This is what Airbnb is working on now. The micro and macroservice hybrid model focuses on the unification of APIs. 
  ![](https://pbs.twimg.com/media/FZKss-fUsAEEhRO.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1554494718498590720))
- Over to you - why do you think both Airbnb and Netflix use GraphQL?
  Reference: https://t.co/nqBncAlnfj 
  ![](https://pbs.twimg.com/media/FZKstp9UsAAlpNY.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1554494730280378368))
