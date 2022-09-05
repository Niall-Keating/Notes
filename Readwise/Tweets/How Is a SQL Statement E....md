# How Is a SQL Statement E...

![rw-book-cover](https://pbs.twimg.com/profile_images/1524184008635998209/vOSCJXuk.jpg)

## Metadata
- Author: [[@alexxubyte on Twitter]]
- Full Title: How Is a SQL Statement E...
- Category: #tweets
- URL: https://twitter.com/alexxubyte/status/1559566919585259520

## Highlights
- How is a SQL statement executed in the database?
  The diagram below shows the process. Note that the architectures for different databases are different, the diagram demonstrates some common designs. 
  ![](https://pbs.twimg.com/media/FaSx2MtUsAEEM4g.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1559566919585259520))
- Step 1 - A SQL statement is sent to the database via a transport layer protocol (e.g.TCP).
  Step 2 - The SQL statement is sent to the command parser, where it goes through syntactic and semantic analysis, and a query tree is generated afterward. 
  ![](https://pbs.twimg.com/media/FaSx2k4VEAABZbz.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1559566927818723328))
- Step 3 - The query tree is sent to the optimizer. The optimizer creates an execution plan.
  Step 4 - The execution plan is sent to the executor. The executor retrieves data from the execution.
  Step 5 - Access methods provide the data fetching logic required for execution 
  ![](https://pbs.twimg.com/media/FaSx3CRVUAAhWML.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1559566935586525184))
- Step 6 - Access methods decide whether the SQL statement is read-only. If the query is read-only (SELECT statement), it is passed to the buffer manager for further processing. The buffer manager looks for the data in the cache or data files. 
  ![](https://pbs.twimg.com/media/FaSx3eWVUAAEY2W.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1559566943044063232))
- Step 7 - If the statement is an UPDATE or INSERT, it is passed to the transaction manager for further processing.
  Step 8 - During a transaction, the data is in lock mode. This is guaranteed by the lock manager. It also ensures the transaction’s ACID properties. 
  ![](https://pbs.twimg.com/media/FaSx36GUUAAQ1KV.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1559566950505672704))
- 👉 Over to you - Which component manages the actual data files? Are there anything important components missing from the diagram? ([View Tweet](https://twitter.com/alexxubyte/status/1559566953894649856))
- I hope you've found this thread helpful.
  Follow me @alexxubyte for more.
  Like/Retweet the first tweet below if you can: https://t.co/B3o3Pljd00 ([View Tweet](https://twitter.com/alexxubyte/status/1559566956658692098))
