---
project: mySmartFlow
date: 04-07-2022
type: internal meeting
---


# Security Sync Meeting (Internal)

### Attendees:
- Niall Keating
- Mike Healy


### Notes:
-   ESP32 security is in the form of secure boot and encrypted flash 
    
    -   Poorly implemented on older chips but better on newer versions 
        
-   This allows you to store secure content in memory, such as certs/keys 
    
    -   Flash is the main important thing for safely storing the key, however secure boot is also important as it prevents rogue firmware from reading flash contents. 
        
-   Can store an X.509 in encrypted flash 
    
-   X.509 certs allow you to use TLS for Mutual Authentication 
    
-   Most important question is around provisioning? 
    
    -   Who do you trust? 
        
    -   Who don't you trust? 
        
    -   What is your threat model? 
        
    -   Do you trust the factory with your certs?  
        
-   For Azure, a unique cert is generated for each device, the hash of the public cert for this cert is stored on Azure. When a challenge is sent up, Azure checks this hash to make sure it matches the one uploaded by the device. 
    
    -   Need infrastructure to generate these keys and post the public hashes to Azure 
        
-   There is no need to sign these certs as azure can be configured not to check the root of trust 
    
    -   Other option here is to configure to use root of trust, then we don't need to save the public hashes