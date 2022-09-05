# We Just Published a YouT...

![rw-book-cover](https://pbs.twimg.com/profile_images/1524184008635998209/vOSCJXuk.jpg)

## Metadata
- Author: [[@alexxubyte on Twitter]]
- Full Title: We Just Published a YouT...
- Category: #tweets
- URL: https://twitter.com/alexxubyte/status/1544711410482966529

## Highlights
- We just published a YouTube video that explains how to store passwords in the database safely.
  If you prefer video format, consider subscribing to our ByteByteGo youtube channel: https://t.co/4HfVP7oLK6
  If you prefer text, you can keep reading:
  𝐓𝐡𝐢𝐧𝐠𝐬 𝐍𝐎𝐓 𝐭𝐨 𝐝𝐨 
  ![](https://pbs.twimg.com/media/FW_q1tCUcAARdfS.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1544711410482966529))
- 🔹 Storing passwords in plain text is not a good idea because anyone with internal access can see them.
  🔹 Storing password hashes directly is insufficient because it is pruned to precomputation attacks, such as rainbow tables.
  🔹 To mitigate this, we salt the passwords. ([View Tweet](https://twitter.com/alexxubyte/status/1544711414597750786))
- 𝐖𝐡𝐚𝐭 𝐢𝐬 𝐬𝐚𝐥𝐭?
  According to OWASP guidelines, “a salt is a unique, randomly generated string that is added to each password as part of the hashing process”. ([View Tweet](https://twitter.com/alexxubyte/status/1544711417239986176))
- 𝐇𝐨𝐰 𝐭𝐨 𝐬𝐭𝐨𝐫𝐞 𝐚 𝐩𝐚𝐬𝐬𝐰𝐨𝐫𝐝 𝐚𝐧𝐝 𝐬𝐚𝐥𝐭?
  1️⃣ A salt is not meant to be secret and it can be stored in plain text in the database. It is used to ensure the hash result is unique to each password. 
  ![](https://pbs.twimg.com/media/FW_q2e5UUAAZyHP.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1544711426018648065))
- 2️⃣ The password can be stored in the database using the following format: 𝘩𝘢𝘴𝘩( 𝘱𝘢𝘴𝘴𝘸𝘰𝘳𝘥 + 𝘴𝘢𝘭𝘵). 
  ![](https://pbs.twimg.com/media/FW_q3DmUIAAlp48.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1544711435325825024))
- 𝐇𝐨𝐰 𝐭𝐨 𝐯𝐚𝐥𝐢𝐝𝐚𝐭𝐞 𝐚 𝐩𝐚𝐬𝐬𝐰𝐨𝐫𝐝?
  To validate a password, it can go through the following process:
  1️⃣ A client enters the password.
  2️⃣ The system fetches the corresponding salt from the database. 
  ![](https://pbs.twimg.com/media/FW_q3lZVUAEdB8X.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1544711444817534977))
- 3️⃣ The system appends the salt to the password and hashes it. Let’s call the hashed value H1.
  4️⃣ The system compares H1 and H2, where H2 is the hash stored in the database. If they are the same, the password is valid. 
  ![](https://pbs.twimg.com/media/FW_q4IjUEAYqSX5.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1544711453797601280))
- Over to you: what other mechanisms can we use to ensure password safety? ([View Tweet](https://twitter.com/alexxubyte/status/1544711457987694592))
