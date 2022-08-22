---
project: Teva
date: 22-08-2022
type: project notes
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

## My Ideas
