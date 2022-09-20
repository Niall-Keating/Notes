# What Does Availability M...

![rw-book-cover](https://pbs.twimg.com/profile_images/1524184008635998209/vOSCJXuk.jpg)

## Metadata
- Author: [[@alexxubyte on Twitter]]
- Full Title: What Does Availability M...
- Category: #tweets
- URL: https://twitter.com/alexxubyte/status/1537100597110792192

## Highlights
- What does Availability mean when you design a system?
  In the famous CAP theorem by computer scientist Eric Brewer, Availability means ​​all (non-failing) nodes are available for queries in a distributed system. 
  ![](https://pbs.twimg.com/media/FVTg2FEUEAIZS7-.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1537100597110792192))
- When you send out requests to the nodes, a non-failing node will return a reasonable response within a reasonable amount of time (with no error or timeout). ([View Tweet](https://twitter.com/alexxubyte/status/1537100601124720643))
- Usually, we design a system for high availability. For example, when we say the design target is 4-9’s, it means the services should be up 99.99% of the time. This also means the services can only be down for 52.5 minutes per year. ([View Tweet](https://twitter.com/alexxubyte/status/1537100603611963392))
- Note that availability only guarantees that we will receive a response; it doesn’t guarantee the data is the most up-to-date.
  The diagram below shows how we can turn a single-node “Product Inventory” into a double-node architecture with high availability. ([View Tweet](https://twitter.com/alexxubyte/status/1537100606170574848))
- 🔹Primary-Backup: the backup node is just a stand-by, and the data is replicated from primary to backup. When the primary fails, we need to manually switch to the backup node.
  The backup node might be a waste of hardware resources. 
  ![](https://pbs.twimg.com/media/FVTg2-WUUAAPJgy.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1537100613976068096))
- 🔹Primary-Secondary: this architecture looks similar to primary-backup architecture, but the secondary node can take read requests to balance the reading load. 
  ![](https://pbs.twimg.com/media/FVTg3fhUUAEUggb.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1537100623237087233))
- Due to latency when replicating data from primary to secondary, the data read from the secondary may be inconsistent with the primary. ([View Tweet](https://twitter.com/alexxubyte/status/1537100627343380480))
- 🔹Primary-Primary: both nodes act as primary nodes, both nodes can handle read/write operations, and the data is replicated between the two nodes. This type of architecture increases the throughput, but it has limited use cases. 
  ![](https://pbs.twimg.com/media/FVTg4L1VUAAPtyh.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1537100635031539718))
- For example, if both nodes need to update the same product, the final state might be unpredictable. Use this architecture with caution! ([View Tweet](https://twitter.com/alexxubyte/status/1537100639041253376))
- If we deploy the node on Amazon EC2, which has 90% availability, the double-node architecture will increase availability from 90% to 99%.
  Over to you: We’ve covered availability, but do these 3 architecture types also guarantee consistency, or not? Let us know your thoughts! ([View Tweet](https://twitter.com/alexxubyte/status/1537100641486589954))
