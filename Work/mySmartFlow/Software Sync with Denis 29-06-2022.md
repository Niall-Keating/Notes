---
project: mySmartFlow
date: 29-06-2022
type: external meeting
---


# Software Sync with Denis

### Attendees:
- Niall Keating
- Marco Pietri
- Denis Murphy
- Dominik


### Notes:
Notes 

-   Logging 
    
    -   Not looking for device to continuously stream logs to the cloud. 
        
    -   Logs should be stored to EEPROM in a FiFo manner 
        
        -   Contents of these logs is to be agreed at a later date 
            
    -   If a device is misbehaving, the cloud will send a cloud to device message requesting logs to be sent 
        
-   Factory Reset 
    
    -   Not looking for this to be done by a button, it should be a software step that is actioned over the service bus or a cloud to device message 
        
-   OTA  
    
    -   Denis was led to believe that OTA over cellular was more difficult, need to follow up on this with Fergal? 
        
    -   Most of their deployments are using cellular  
        
-   Cloud 
    
    -   Like the option of being cloud agnostic in the future 
        
    -   Using Azure for now 
        
    -   This leaves DeviceTwin functionality up in the air, we can recommend something in this regard 
        
-   SIMs 
    
    -   Using ESAY? sims at the moment 
        
    -   Evaluating Autonomo? SIMs and potentially looking to use themng Autonomo? 
        
    -   Want to be able to configure the APN remotely  
        
-   Discussion on Auth 
    
    -   TPM is preferred solution 
        
        -   Understands could be costly 
            
    -   Needs to see BOM to decide if they will go for it  
        
    -   When we know about TPM cost we can talk about Auth again 
        
    -   Feels SAS tokens are least secure of 3 options 
        
-   Provisioning: 
    
    -   Wants an option for auto provisioning so that they don't have to flash keys to EEPROM  
        
    -   Again we need to understand auth before making recommendations here. 
        

Internal Notes after the call 

-   I think we should look at using Espressif components for modem and Azure SDK?