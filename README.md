# MFT-REST
A REST API wrapper for the MFT Command Line Client (AdminClient)

## Purpose:
The project creates a REST API interface to call all the same commands that are available from the AdminClient.  This allows application developers an easier means to interact and manage resources in TIBCO Managed File Transfer.

## Pre-requisites
The project is written with Windows in mind.  That's not to say it can't be modified to work with Linux, just that it was not my priority in this first release.

### Software Required:
* TIBCO BusinessWorks 6
* MFT Command Center

## Environment Setup
* Install AdminClient on same server as BW engine.  (It is not necessary to install the AdminClient on the same server as MFT)  
  Run through the AdminClient setup  
  `java cfcc.Config`  
  Keep in mind all the Command Actions will be carried out by the MFT ID provided in this configuration step, and will be limited by the permissions as defined in MFT.
* Import the BW application into the BusinessWorks Studio.
* Deploy the BW application, REST-CLI, to TIBCO Enterprise Administrator.
* Set the module properties
  * cmd - Defines the full path to the cfcc.bat file  
    e.g. c:\apps\AdminClient\cfcc.bat
  * workingDir - Defines the full path to the root directory of the AdminClient  
    e.g. c:\apps\AdminClient

Once deployed, obtain the restDoc URL from TEA to test out the REST API.