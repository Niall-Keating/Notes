---
project: mySmartFlow
date: 02-08-2022
type: external meeting
---


# Project Kickoff Meeting

### Attendees:
- Niall Keating
- Dave Hogan
- Denis Murphy
- Dominik


### Notes:
-   V3's is SAMD and SIMCom 
    
-   In relation to V3 Firmware, they would be looking for: 
    
    -   RTOS Support 
        
    -   Azure SDK 
        
    -   LWIP/Cyclone network stack on MCU  
        
-   The V3 uses the SIMComm 868E module 
    
-   Denis's email today is in relation to 100-200 V4's 
    
    -   Other supplier is saying they can source 100 or 200 ESP32's 
        
    -   Need to source modems  
        
    -   This would give them a breather to purchase remaining at the long lead times 
        
    -   Need to know plan by the end of this week at the latest 
        
-   SIMs: 
    
    -   Using [Eseye SIMs](https://www.eseye.com/iot-solutions/anynet-iot-sim-card/) at the moment 
        
    -   Moving to [Monogoto SIMs](https://monogoto.io/secure-iot-sim/) 
        
        -   Gives them control of SIM Keys 
            
-   V3 FOTA is vis FTP 
    
    -   This needs to be improved to a better / more secure mechanism. 
        
-   What is a DeviceTwin? 
    
    -   Interval Configurations  
        
    -   NTP server 
        
    -   Valves state 
        
    -   Centre button 
        
    -   SW debounce interval 
        
        -   0 would mean no debounce 
            
    -   Should have UTC for time fallback 
        
        -   *** This is a bad idea, would result in constant updates to device twin 
            
        
-   What is Device to Cloud? 
    
    -   Hourly Sensor Uploads 
        
-   Ability to update APN over Field Service Bus