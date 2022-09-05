# A Cloudflare Outage Knoc...

![rw-book-cover](https://pbs.twimg.com/profile_images/1524184008635998209/vOSCJXuk.jpg)

## Metadata
- Author: [[@alexxubyte on Twitter]]
- Full Title: A Cloudflare Outage Knoc...
- Category: #tweets
- URL: https://twitter.com/alexxubyte/status/1539274640975048704

## Highlights
- A Cloudflare outage knocked many popular services such as Udemy, Coinbase, Discord, etc., offline. What happened?
  Cloudflare wrote an incident report. Here is my TLDR after reading the report.
  Image source (you can also read the whole report here): https://t.co/z2FpcOkIbA 
  ![](https://pbs.twimg.com/media/FVyaIHKUcAM7nXK.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1539274640975048704))
- 1. A new routing layer called “spin” is added to improve reliability and maintainability. 
  ![](https://pbs.twimg.com/media/FVyaIhRUYAE7HPg.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1539274649879490560))
- 2. As part of the BGP protocol, terms are defined to define what IP addresses (prefixes) are accessible by the internet. Due to the reordering of terms, a critical subset of prefixes is withdrawn. Those IP addresses are no longer accessible. 
  ![](https://pbs.twimg.com/media/FVyaJA9UcAAyWGn.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1539274658146422784))
- 3. Due to this, engineers are not able to reach affected locations to revert problematic changes.
  4. Backup procedures were used to take control of the affected locations.
  Handling a service outage is stressful. Good job by the Cloudflare team for fixing the outage quickly. ([View Tweet](https://twitter.com/alexxubyte/status/1539274661845839872))
