# Intro
Based on [[Cloud Sync]] we decided not to develop a new cloud app for the Teva device to upload it's data to as a lot of the functionality is already build into the DMS. In order to get the functionality that the hardware guys are looking for, we will need to extend the functionality inside of the session endpoint to store the inhaler sample data to thingsboard. The local test app running the test on the inhaler will then poll the DMS to pullthis data down locally. 

## DMS changes required
1. Modify the `/<IMEI>/session` view to save the sample data uploaded by the teva device to thingsboard
2. 
