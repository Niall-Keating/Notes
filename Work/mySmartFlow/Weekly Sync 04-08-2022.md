---
project: mySmartFlow
date: 04-08-2022
type: external meeting
---



# Weekly Sync 04-08-2022 (External)

Attendees:
- Niall
- James
- Fergal
- Dave
- Denis
- Dominik


Notes:
-   SmartFlow interested in Taoglas offer to do manufacturing of V2 boards in order to get access to existing stock. 
    
    -   This depends on services being offered and the cost 
        
    -   Taoglas will prep a 200pc build, James will provide a quote for this when he is abck next week. 
        
-   [FB] Proposed the idea of using RS232 as the physical layer of the service bus. This will be placed as a footprint, will be optional component to place  
    
    -   Regardless there will be TVS diaodes for ESD protection 
        
    -   No problems with this from SmartFlow POV 
        
-   [FB] All I/O lines should have TVS diodes for ESD protection purposes 
    
    -   No issues from SmartFlow POV 
        
-   [FB] Raised issues with current battery circuitry, no over temp protection, constant charge will impact battery performance over time.  
    
    -   Taoglas are proposing a redesign of battery circuitry to include a charge controller IC and move to Lithium Polymer batteries 
        
    -   SmartFlow are okay with Taoglas proceeding with this redesign  
        
-   [DM] Noted that previous communications in relation to the link wire used on the opto isolator on flow sensor input were incorrect 
    
    -   Negated input is tied to 5V not GND 
        
    -   [FB] recommends keeping this circuitry as is, this allows the Hub to use flow meters with external PSU without tieing in external GND. 
        
    -   [DM] SmartFlow happy to keep this circuitry as is. 
        
-   [DM] Raised point of reset/power button which was discussed previously 
    
    -   Number of options we can use to progress this: 
        
        -   Hall Effect so magnet can be used to power-cycle/reset the Hub.  
            
        -   Reuse the existing alarm connections on the baseboard to add a button externally 
            
        -   Place a reset putton on the main board and modify the plastics 
            
    -   [FB] Will place footprint for reset button on mainboard as well as include option to reuse alarm switch on baseboard, so that two options are available.  
        
-   [FB] Raised issues observed with existing battery connector being easily pulled of PCB 
    
    -   [DM/DH] Not tied into this connector, Taoglas can choose what to do with it.

Actions:
-   [FB/AB/NK] to proceed with plan for 200 V4 build, James will provided a quote for this when he is back next week 
    
-   [PT/FB] will update HW: 
    
    -   Footprint for RS-232 IC with option to bypass if not placed 
        
    -   All I/O lines to have TVS diodes for ESD protection 
        
    -   Redesign battery charge circuitry as agreed with SmartFlow 
        
    -   Add Footprint for reset button, need to clarify whether we power cycle or do MCU reset 
        
    -   Redo alarm circuitry going to baseboard to support dame reset mechanism as above