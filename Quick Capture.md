# Quick Capture

- Don't respond immediately, write it down here...


## Thoughts on overall process in engineering
- As it stands we manufacture hardware in a factory in Shannon and it is often a  nightmare for many reasons
	- EVT ssoftware is linux and requires too much configuration, should be able to just have a QR or a single button to click that starts the test and knows everything
	- everything is stored to a csv file
		- failed devices aren't populated
	- Lots of manual processes
		- I have to copy out public keys and imei's and paste into new file
		- go to instance
		- creare a configuration for a device if it doesn't exist
		- use the above conf file and csv to provision the batch of devices
		- 
- We need something better than a CSV file
	- I think mongodb
		- We can have required keys, ie SN, manu date etc
		- Then an object that can change between devices and contains public key and other device/product specific options
- We need a central serive which allows us to view all of the devices we manufature via a web portal
	- THIs portal should allow
		- Webhook to send to customer
		- Export option for csv, excel etc
		- NOtes section to store notes on device?
		- API to pull out from dms instance
			- or possibly an option to push to an instance
- Binaries when built on ci/cd should be pushed to bintray or something, builds are tagged and an api on cloud that auto discovers only builds it can use with correct urls etc
- owners for each sections, 
	- i.e. factory sw is owned by:
		- Operations
		- Engineering Manager
		- HW Lead
		- SW LEad
	- cloud software is owned by
		- ENg Manager
		- SW Team lead
		- SW Team
		- devops/infrastructure
	- Firmware is owned by
		- PMO
		- ENgineering Manager
		- SW Team Lead(s)
		- Firmware team
	- CI/CD Infrastreuctr
		- SW TEam Lad
		- Validation Team
		- Devops
		- 


## Things we need
- Branching strategy
- rules to only allow SM's when we have a flow diagram
- Platform IO
- Linux image
- single IDE
- place to store binaries
- docker
- aws monitoring on grafana/prometheus
- APN list file that matches IMSI prefix... common across all devices
- 