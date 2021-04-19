# CS2-CL
CalSim II-CalLite wresl script updates based on CSII study corroboration with the Delivery Capability Report (DCR) 2019

## Steps
Following is a step-by-step guide for using the CS2CL Tool to create a CalLite SV file from a CalSim study. An existing conditions study (F-Part = 2020D09E) is used for example. 
1)	Run CalSim, save the DV file as 2020D09EDV.DSS (for example).
2)	Copy 2020D09EDV.DSS and re-save as 2020D09EDVSV.DSS
3)	Open this new DVSV.DSS file in HEC-DSSVue and drag and drop the 2020D09ESV.DSS file into the list of timeseries. Click “Copy All”.
4)	Repeat Step #3 to copy the timeseries over from “Other_timeseries_2020D09E”. (See additional notes)
5)	Ensure the correct pathnames are used in CS2CL_study.config. The run period should be set to Oct 1920 – Sept 2004. 
6)	Run the CS2CL tool by double clicking on CS2CL_run.bat.  It will output a DV timeseries for use as a SV input timeseries in CalLite..   


## Additional notes:

1. After combining together CalSim SV and DV files, also have to add in the following timeseries from the DSS files Other_timeseries_2020D09E.dss or Other_timeseries_2005A01A.dss:
* REST_REQ_NP_F
* REST_REQ_NP_I
* REST_REQ_P_F
* REST_REQ_P_I
* UNIMPAIRED_NDO
* UNIMPAIRED_SAC
* UNIMPAIRED_SJR

2. CS2CL model needs to be run from Oct 1920 - Sep 2004.

