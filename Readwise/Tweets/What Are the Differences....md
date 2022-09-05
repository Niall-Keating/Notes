# What Are the Differences...

![rw-book-cover](https://pbs.twimg.com/profile_images/1524184008635998209/vOSCJXuk.jpg)

## Metadata
- Author: [[@alexxubyte on Twitter]]
- Full Title: What Are the Differences...
- Category: #tweets
- URL: https://twitter.com/alexxubyte/status/1547610261070090242

## Highlights
- What are the differences between 𝐛𝐚𝐫𝐞 𝐦𝐞𝐭𝐚𝐥, 𝐯𝐢𝐫𝐭𝐮𝐚𝐥 𝐦𝐚𝐜𝐡𝐢𝐧𝐞𝐬, or 𝐜𝐨𝐧𝐭𝐚𝐢𝐧𝐞𝐫𝐬? When deploying a modern application stack, how do we decide which one to use?
  You can watch it here:
  https://t.co/9qgBqw7QZ9
  If you prefer text, keep reading: 
  ![](https://pbs.twimg.com/media/FXo3VDmVQAM3bWQ.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1547610261070090242))
- 𝐁𝐚𝐫𝐞 𝐦𝐞𝐭𝐚𝐥
  The granddaddy of these is bare metal. A bare metal server is a physical computer that is a single tenant only.
  Bare metal gives us complete control over the hardware resources and the software stack to run. 
  ![](https://pbs.twimg.com/media/FXo3VdeUcAMMcC4.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1547610270113026048))
- For software applications that require the absolute highest performance from the hardware, bare metal could be a good way to go.
  Bare metal servers are physically isolated.
  𝐁𝐞𝐧𝐞𝐟𝐢𝐭𝐬:
  ✅ First, it is not affected by the noisy neighbor problem. ([View Tweet](https://twitter.com/alexxubyte/status/1547610273946542081))
- ✅ Second, the isolation provides the highest level of security.
  𝐃𝐨𝐰𝐧𝐬𝐢𝐝𝐞:
  🚫 Bare metal is expensive, hard to manage, and hard to scale. ([View Tweet](https://twitter.com/alexxubyte/status/1547610276593143813))
- 𝐕𝐢𝐫𝐭𝐮𝐚𝐥 𝐦𝐚𝐜𝐡𝐢𝐧𝐞
  A virtual machine is the emulation of a physical computer. This is called virtualization.
  Running on top of the host operating system is a special piece of software called a hypervisor. This is also known as a virtual machine monitor. 
  ![](https://pbs.twimg.com/media/FXo3WSUVEAITmyU.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1547610283828400137))
- The hypervisor manages virtual machines. It creates an abstraction layer over the hardware, so that multiple operating systems can run alongside each other. ([View Tweet](https://twitter.com/alexxubyte/status/1547610287271841794))
- Each virtual machine has its own guest operating system. On top of each guest operating system runs the applications for a tenant.
  𝐁𝐞𝐧𝐞𝐟𝐢𝐭𝐬:
  ✅ Virtual machines are cheaper to run.
  ✅ They are easier to scale.
  𝐃𝐨𝐰𝐧𝐬𝐢𝐝𝐞: ([View Tweet](https://twitter.com/alexxubyte/status/1547610289780056065))
- 🚫 Virtual machines could be vulnerable to the noisy neighbor problem. ([View Tweet](https://twitter.com/alexxubyte/status/1547610292346966019))
- 𝐂𝐨𝐧𝐭𝐚𝐢𝐧𝐞𝐫𝐬
  A container is a lightweight and standalone package of an application with all its dependencies like libraries, frameworks, and runtime. Containerization is considered to be a lightweight version of virtualization. 
  ![](https://pbs.twimg.com/media/FXo3XMqUYAUVZIT.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1547610299687002115))
- 𝐁𝐞𝐧𝐞𝐟𝐢𝐭𝐬:
  ✅ The container engine provides even faster resource provisioning.
  ✅ Containers are scalable and portable.
  ✅ Since each container runs as a native process of the host operating system, they are much faster to start. ([View Tweet](https://twitter.com/alexxubyte/status/1547610303315075072))
- ✅ All these make containers even easier to deploy and maintain at scale. ([View Tweet](https://twitter.com/alexxubyte/status/1547610305865273344))
- 𝐃𝐨𝐰𝐧𝐬𝐢𝐝𝐞:
  🚫Potentially less secure
  In conclusion, system design is about tradeoffs. It is no different when it comes to bare metal, virtual machines and containers. There is no single right answer. ([View Tweet](https://twitter.com/alexxubyte/status/1547610308432130051))
- Overall to you: What comes after containers? Serverless and edge computing come to mind. They make the developer productivity and deployment stories even more compelling, but with their own sets of tradeoffs. What are the tradeoffs? ([View Tweet](https://twitter.com/alexxubyte/status/1547610311020097537))
