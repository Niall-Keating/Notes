## Notes

Process: 

-   SmartFlow get a signed CA Root Cert 
    
-   Gernerate an intermediate signer cert 
    
-   Upload signer cert to the DPS 
    
-   Above intermediary cert is then used to create another signer cert that can be sent to the factory  
    
-   Factory then uses the above signer to generate leaf certs which are saved to secure flash on the ESP32 
    
-   The ESP32 contacts the DPS and provides the cert chain to ensure proof of possession  
    
-   DPS checks certs are valid and ensures proof of posession 
    
-   DPS assigns IoT Hub based on Enrollment group, or if there is a specific enrolmment for device this supercedes


## Links
[https://docs.microsoft.com/en-us/azure/iot-dps/concepts-x509-attestation](https://docs.microsoft.com/en-us/azure/iot-dps/concepts-x509-attestation) 

[https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates](https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates) 

[https://docs.microsoft.com/en-us/azure/iot-dps/concepts-service#enrollment-group](https://docs.microsoft.com/en-us/azure/iot-dps/concepts-service#enrollment-group) 

[https://docs.microsoft.com/en-us/azure/iot-dps/quick-create-simulated-device-x509?tabs=linux&pivots=programming-language-ansi-c](https://docs.microsoft.com/en-us/azure/iot-dps/quick-create-simulated-device-x509?tabs=linux&pivots=programming-language-ansi-c) 

[https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-concept](https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-concept)

