---
project: mySmartFlow
date: 27-06-2022
type: internal meeting
---


# Internal Sync

### Attendees:
- Niall Keating
- Marco Pietri
- James Addie
- Adrian Burns


### Notes:
-   Redesigning the product to use the ESP32   
-   We need to work with them to figure requirements for the firmware 
    -   We need to gather these 
-   JA: Key is plan from POC to Production 
-   They aren't licensing the Taoglas/BSP/Framework 
-   They need to map out what they want included in the firmware 
    -   Gather fully and work though requirements with them   
-   We've identified ESP32 as MCU, hardware team are working to design this in 
    -   They need to decide whether  
-   They could potentially change to a Thales modem or whatever they want, Fergal might know this 
    -   LTE vs NB-IoT vs CAT-M 

-   Do they need an RTC? 
    
-   No Battery? 
    
-   Watchdog, don't have this currently? 
    
-   Did they give us any units? 
    
    -   Sensors/Actuators 
        
-   ESP32 in existing V2/V3 code was a POC, can be ignored 
    
-   WiFI/BLE do they need this? 
    
-   SIM Cards? 
    
-   Pull out doc similar to BSCi document for block diagram 
    

As Requirements Q's: 

-   Requirements: 
    
    -   Sensor control 
        
    -   Device management 
        
        -   Fota 
            
    -   Connectivity 
        
    -   Diagnostics 
        
    -   BLE/Lora