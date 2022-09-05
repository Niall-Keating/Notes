# Do You Know the James We...

![rw-book-cover](https://pbs.twimg.com/profile_images/1524184008635998209/vOSCJXuk.jpg)

## Metadata
- Author: [[@alexxubyte on Twitter]]
- Full Title: Do You Know the James We...
- Category: #tweets
- URL: https://twitter.com/alexxubyte/status/1551222152497483776

## Highlights
- Do you know the James Webb Space Telescope (JWST) uses an 𝐞𝐯𝐞𝐧𝐭-𝐝𝐫𝐢𝐯𝐞𝐧 architecture for its operations?
  Disclaimer: This post reflects my understanding of the paper: JWST: Maximizing Efficiency... by the Space Telescope Science Institute. For details, refer to [1]. 
  ![](https://pbs.twimg.com/media/FYcMUkgVsAA-3IP.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1551222152497483776))
- The diagram below shows the architecture.
  Step 1: When the observation plans are designed for JWST, the team needs to come up with a proposal. The proposal is broken up into scheduling units called ‘Visits.’ Each Visit has a corresponding observing window. 
  ![](https://pbs.twimg.com/media/FYcMVOlVQAQrMvR.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1551222164816158720))
- These Visits can build a long-range plan, which is about one year in duration, or a short-range plan, which is about 22 days in duration. The plans are called an Observation Plan [1]. ([View Tweet](https://twitter.com/alexxubyte/status/1551222168570105856))
- Step 2: These Observation Plans are processed by high-level onboard scripts, called the Observation Plan Executive (OPE). The OPE passes the activity parameters from the time-ordered Visits to lower-level onboard scripts. [1] 
  ![](https://pbs.twimg.com/media/FYcMWEdUYAA6vJg.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1551222178938380296))
- Step 3: The activity onboard scripts construct the commands and telemetry requests in real-time, onboard the JWST. [1] 
  ![](https://pbs.twimg.com/media/FYcMWwAUsAAFSmE.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1551222191554908160))
- Step 4: When a command is issued, these lower-level scripts evaluate the telemetry response and pass the script status up to the OPE. Based on the script status, the OPE can skip Visits. [1] 
  ![](https://pbs.twimg.com/media/FYcMXfIUUAAjGfv.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1551222203076599808))
- Compared with the Hubble Space Telescope (HST), JWST science operations are driven by onboard scripts written in customized Javascript, not in binary command blocks. This abstraction forms an event-driven architecture and makes operational decisions based on telemetry responses. ([View Tweet](https://twitter.com/alexxubyte/status/1551222207006658562))
- The OPE can:
  🔹 Skip Visits based on script status
  🔹 Add Visits to the end of the Plan
  🔹 Remove Visits to redefine the end of the Plan
  🔹 Stop the Plan after a specified Visit or stop the entire plan ([View Tweet](https://twitter.com/alexxubyte/status/1551222209493942273))
- In this way, one failure doesn’t hurt the entire Plan. JWST can continue with the rest of the Plan. This maximizes efficiency and resilience.
  Over to you: How to engineer and test mission-critical software?
  Reference:
  [1] https://t.co/BHxfsVQL9C ([View Tweet](https://twitter.com/alexxubyte/status/1551222211972763649))
