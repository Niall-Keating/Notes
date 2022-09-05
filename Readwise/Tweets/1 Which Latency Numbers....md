# /1 Which Latency Numbers...

![rw-book-cover](https://pbs.twimg.com/profile_images/1524184008635998209/vOSCJXuk.jpg)

## Metadata
- Author: [[@alexxubyte on Twitter]]
- Full Title: /1 Which Latency Numbers...
- Category: #tweets
- URL: https://twitter.com/alexxubyte/status/1564640354690670592

## Highlights
- /1 Which latency numbers we should know?
  Please note those are not accurate numbers. They are based on some online benchmarks (Jeff Dean’s latency numbers + some other sources). 
  ![](https://pbs.twimg.com/media/Fba4G-HUEAE4-9t.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1564640354690670592))
- /2 🔹L1 and L2 caches: 1 ns, 10 ns
  E.g.: They are usually built onto the microprocessor chip. Unless you work with hardware directly, you probably don’t need to worry about them. 
  ![](https://pbs.twimg.com/media/Fba4HXjUEAAShKG.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1564640363268042752))
- /3 🔹RAM access: 100 ns
  E.g.: It takes 100 ns to read data from memory. Redis is an in-memory store, so it takes about 100 ns to read data from Redis
  🔹Send 1K bytes over 1 Gbps network: 10 us
  E.g.: It takes around 10 us to send 1KB of data from Memcached through the network 
  ![](https://pbs.twimg.com/media/Fba4H33UEAAwnaE.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1564640371904090113))
- /4 🔹Read from SSD: 100 us
  E.g.: RocksDB is a disk-based K/V store, so the read latency is around 100 us on SSD. 
  ![](https://pbs.twimg.com/media/Fba4IYrUcAAntLG.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1564640380791840768))
- /5 🔹Database insert operation: 1 ms.
  E.g.: Postgresql insertion might take 1ms. The database needs to store the data, create the index, and flush logs. All these actions take time. 
  ![](https://pbs.twimg.com/media/Fba4I55VUAAFGvn.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1564640389788667904))
- /6 🔹Send packet CA->Netherlands->CA: 100 ms
  E.g.: If we have a long-distance Zoom call, the latency might be around 100 ms. 
  ![](https://pbs.twimg.com/media/Fba4JaOUUAEDCVg.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1564640398055682050))
- /7 🔹Retry/refresh internal: 1-10s
  E.g: In a monitoring system, the refresh interval is usually set to 5~10 seconds (default value on Grafana).
  Notes
  -----
  1 ns = 10^-9 seconds
  1 us = 10^-6 seconds = 1,000 ns
  1 ms = 10^-3 seconds = 1,000 us = 1,000,000 ns 
  ![](https://pbs.twimg.com/media/Fba4J40UEAEeY2a.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1564640407107026948))
- /8 Over to you - 1). Do you know all 😊?
  2). Nowadays, disk and tape are used as data backup. Do you know which one has a higher write speed?
  👉 Enjoyed this post? You might like our weekly System Design Newsletter as well. Subscribe here:
  https://t.co/dkjDPxrTOt 
  ![](https://pbs.twimg.com/media/Fba4Kc0UIAAwjxA.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1564640417651404801))
- The goal of the diagram is not to get the numbers accurate, but to get a general sense of what is slow and fast, in relative terms. We hope the numbers are within the 1 order of magnitude error range. Let me know if you spot an error! I'll correct it. Thank you. ([View Tweet](https://twitter.com/alexxubyte/status/1564658926355853312))
