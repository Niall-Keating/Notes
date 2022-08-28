---
project: Teva
date: 24-08-2022
type: project notes
tags: [Thingsboard, DMS, AWS, Teva, JSON, session-endpoint, updates-endpoint, FT232, GPIO, UI]
---

# Intro
Based on [[Cloud Sync]] we decided not to develop a new cloud app for the Teva device to upload it's data to as a lot of the functionality is already build into the DMS. In order to get the functionality that the hardware guys are looking for, we will need to extend the functionality inside of the session endpoint to store the inhaler sample data to thingsboard. The local test app running the test on the inhaler will then poll the DMS to pull this data down locally. 

## DMS changes required
1. Modify the `/<IMEI>/session` view to save the sample data uploaded by the teva device to thingsboard
	- Use `/<IMEI>/updates` view as a reference for how to save telemetry to Thingsboard
	- See [Github](https://github.com/taoglas-iot/device_manager/blob/5c7e818da01377c1066fb13dfa7ffd2723b59299/api/data_pipeline.py#L60-L78) for reference on how to use the Thingsboard adapter
	- The following keys from the uploaded JSON should be saved:
		- `bat_mv`
		- `pres_min`
		- `duration_ms`

## Test Application Design
2. Use Python to create a test application that will run the local Inhaler tests. 
	- This will use the FT232H driver to interact with GPIO and read logs from the devices
	- Write to the GPIO on the Smart Inhaler to simulate the cap being opened and closed on the inhaler. Record the time of this interaction
	- Wait `X` minutes and then use the EDGE Insights API to pull in the latest samples for the DUT, if the sample timestamp is equal to or greater than the time the interaction was triggered, save the lines to a local database and display the samples on the table view
	- Delay `X` minutes and repeat the test steps(This should be an interrupt or a cron)
	- If the next GPIO interaction is scheduled to take place but the previous samples have not been uploaded, mark the previous test as failed/incomplete.

## Tasks 
- [ ] Create sequence diagram🛫 2022-08-29 🔼 


## Architecture 
![[test_app_v2_arch.excalidraw.png]]

## Test App Design
![[test_app_design.excalidraw]]