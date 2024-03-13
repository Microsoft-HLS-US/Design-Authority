# Design Authority
 Design Authority Booking Application

## Description

Included is a starter solution that allows organizations to manage their project intake, review scheduling process. 

## Installation

1. Ensure that SharePoint folder for Project Intake file drop is created. 
2. Ensure folder structure for Report generation is created in OneDrive for Business. Suggested structure below.
	* Company
		* Templates
		* Outputs
			* Word
			* PDF
3. Copy the Report word template to the \Company\Templates folder. 
4. Import the Calendar PCF managed solution and publish it (https://github.com/rwilson504/PCFControls/tree/master/Calendar). 
5. Import the Color Picker PCF managed solution and publish it (https://github.com/rwilson504/PCFControls/releases/latest/download/ColorPicker_managed.zip)
6. Import the unmanaged solution zip file to your Dataverse environment and publish all customizations. 
7. Import the Control Table Data through Power Apps Maker Portal > Tables > Control > Command menu item (Import)
8. Import the flow packages and publish all customizations. You will be asked to create connections. 
	* Dataverse
	* Outlook
	* Word
	* Excel
	* Entra
	* OneDrive
	* SharePoint
9. Edit the "Import Incoming DA Intake File" flow's trigger location to point to the SharePoint folder(from Step 1). 
10. Edit the "Send Report to Roster Members"  flow's "Populate Word Template" action to point to the Report word template (from step 3)
11. Update Control table record titled "Roster" to the GUID for the Distribution list from Entra. The MDA can be used to edit this value. 
12. Update the verbiage(s) for the outbound email. Ensure that tokens in double curly braces are not deleted. 

## License

MIT License

Copyright (c) [2024] [Abhijeet Premkumar]

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.