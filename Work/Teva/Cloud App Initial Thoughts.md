---
project: Teva
date: 22-08-2022
type: project notes
tags: [EDGE Insights, DMS, AWS, Cloud App, FT232H]
---

# Background
- Fergal wants an app to cofirm that a DUT has uploaded it's samples successfully. 
- Will be using a FT232H dev-kit locally to:
	- Act as a switch
	- Detect super cap charge state?
	- Read logs
	- NK note: we have a Python driver for this already as part of EVT app. 
- DUT will run long term in the lab, cap open will be triggered perioidically, in theory samples will be uploaded to the cloud 
- Our app should confirm stats of ...
- Two pieces of sw required, one to run locally and one in the cloud


## My Research
 - Teva repo:
 - Looks like was a MQTT client at one stage
 - Now using file upload endpoint instead?
 - links:
 - The `/v1/<IMEI>/session/ ` endpoint us used to upload a JSON file an example of which can be viewed below:
``` JSON
{
   "serial":"352656100817447",
   "sample_count":"1.0",
   "rssi":"-110.0",
   "timestamp":"2022-06-30_13:05:32",
   "samples":[
      {
         "epoch":"1656594307.0",
         "bat_mv":"3563.0",
         "pres_min":"429.72",
         "duration_ms":"1406.0"
      }
   ]
}
```
- The files uploaded to the `session` endoint are saved to an internal `/media` folder on the cloud platform, for the Teva SmartInhaler testing that Pawel J has been conducting recently, this can be found at: `/var/www/firmwave-staging/media` 
- A log file showing this transaction was sent by Pawel and is available here: ![[Teva_Logs_30-06-22-15h17m.txt]]


## My Ideas
- Python webserver that runs locally, connects to the FTDI over web serial(if we don't need direct GPIO)
- either a new simple webserver othat accepts the requests from the device
	- or reuse the existing DMS and use the API to poll somehow? 

## Architecture

![[test_app_arch.excalidraw.png]]

1. Cloud App
2. Laptop running test planner
	- Controls the FT232
	- Reads samples from cloud(Asyn or Sync)
3. Teva SmartInhaler 
4. LTE-M link to public internet/cloud