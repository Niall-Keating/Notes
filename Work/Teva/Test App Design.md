# Intro
Based on [[Cloud Sync]] we decided not to develop a new cloud app for the Teva device to upload it's data to as a lot of the functionality is already build into the DMS. In order to get the functionality that the hardware guys are looking for, we will need to extend the functionality inside of the session endpoint to store the inhaler sample data to thingsboard. The local test app running the test on the inhaler will then poll the DMS to pullthis data down locally. 

## DMS changes required
1. Modify the `/<IMEI>/session` view to save the sample data uploaded by the teva device to thingsboard
	- Use `/<IMEI>/updates` view as a refernece for how to save teleemetry to Thingsboard
	- See [Github](https://github.com/taoglas-iot/device_manager/blob/5c7e818da01377c1066fb13dfa7ffd2723b59299/api/data_pipeline.py#L60-L78) for reference on how to use the Thingsboard adapter
	- The following keys from the uploaded JSON should be saved:
		- `bat_mv`
		- `pres_min`
		- `duration_ms`
2. Use Python to create a test application that will run the local i

## Tasks 
- [ ] Create sequence diagram🛫 2022-08-29 🔼 


## Architecture 
![[test_app_v2_arch.excalidraw.png]]

## Test App Design
![[test_app_design.excalidraw]]