---
project: mySmartFlow
date: 29-06-2022
type: external meeting
---


# Project Kickoff Meeting

### Attendees:
- Niall Keating
- Marco Pietri
- Denis Murphy
- Dominik


### Notes:
Notes: 

-   Water usage monitoring 
    
-   Uploading usage data to cloud 
    
-   One of the biggest things for them is sustainability 
    
-   Think of it as a Smart water monitoring platform 
    

Marco – How often collect and upload and send data 

-   Pulse counter on meter 
    
-   Upload once per hour 
    
    -   Contains a single value which is the count of the pulses 
        
    -   NK Q: does cloud map pulses to the flow rate? 
        

Fergal – Battery backup 

-   Yes as per V2 
    

Fergal – Antenna Team, situations with poor signal coverage?  

-   2 devices in Dundrum town centre struggling with RF 
    
-   They are using an external antenna 
    
-   Underground in carpark in most circumstances 
    

Marco – What are the main hardware issues? 

-   Biggest issue is cellular connectivity and staying connected 
    
-   When reconnecting, it can end up in a locked state that requires a restart 
    
-   Need a button to power switch to restart 
    
-   REQUIREMENT: WATCHDOG 
    
-   The device should be well able of recovering itself 
    
-   Some meter's don’t always return a nice square-wave 
    
    -   Software debounce? 
        
    -   Hardware debounce is preferable on Fergal's side 
        
-   Fergal want's some kind of hardware restart instead of watch dog 
    
-   Local logging? No – cloud logging 
    
    -   Need to clarify what they expect from logging? 
        

Fergal – WiFi back up? 

-   Dave shot this one down 
    

Denis sharing his requirements doc, this is the one we were looking at yesterday 

-   Time – Fergal – ESP32 has an RTC 
    
-   Item 2:  
    
    -   Cloud wants to be able to request flow for a date and time 
        
    -   Ie store 1/3/6 months of data on the device and then allow cloud to pull this 
        
-   Need ability for partial/real time flow readings 
    
    -   To help engineers on install process 
        
    -   Fergal wants to do a cable? 
        
    -   I think BLE? 
        
-   Valves 
    
    -   Ground 
        
    -   Input to open valve 
        
    -   Input to close valve 
        
    -   Pin to check if valve is open or codes 
        
    -   5 valve positions 
        
        -   Commissioning just opens/closes all valves and checks status 
            
        -   If valve is in-between it will report unknown 
            
    -   Ability to open/close manually 
        
        -   Current firmware doesn't implement functionality to periodically check the valve states 
            
        -   They would like this  
            
        -   Poll 30 mins/60 mins 
            
        -   Fergal proposing all times should be configurable 
            
-   Sw reset of device is currently implemented, this needs to be retained 
    
-   Centre button – hold for 3 seconds 
    
    -   Close valves 
        
    -   Next time button is held, open valves