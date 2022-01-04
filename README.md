# XenAppXenDesktop7V1
	Creates an inventory of a Citrix XenDesktop 7.0 through 7.7 Site using Microsoft 
	PowerShell, Word, plain text, or HTML.
	
	This script requires at least PowerShell version 3 but runs best in version 5.

	Word is NOT needed to run the script. This script outputs in Text and HTML.
	
	You do NOT have to run this script on a Controller. This script was developed and run 
	from a Windows 8.1 VM.
	
	You can run this script remotely using the -AdminAddress (AA) parameter.
	
	This script supports versions of XenApp/XenDesktop from 7.0 to 7.7. 

	If you are running XA/XD 7.8 through CVAD 2006, please use:
	https://carlwebster.com/downloads/download-info/xenappxendesktop-7-8/

	If you are running CVAD 2006 and later, please use:
	https://carlwebster.com/downloads/download-info/citrix-virtual-apps-and-desktops-v3-script/

	If you are running Citrix Cloud, please use:
	https://carlwebster.com/downloads/download-info/citrix-cloud-citrix-virtual-apps-and-desktops-service/
	
	By default, only gives summary information for:
		Administrators
		Applications
		Delivery Groups
		Hosting
		Logging
		Machine Catalogs
		Policies
		StoreFront

	The Summary information is what is shown in the top half of Citrix Studio for:
		Machine Catalogs
		Delivery Groups
		Applications
		Policies
		Logging
		Administrators
		Hosting
		StoreFront

	Using the MachineCatalogs parameter can cause the report to take a very long time to 
	complete and can generate an extremely long report.
	
	Using the DeliveryGroups parameter can cause the report to take a very long time to 
	complete and can generate an extremely long report.

	Using both the MachineCatalogs and DeliveryGroups parameters can cause the report to 
	take an extremely long time to complete and generate an exceptionally long report.

	Creates an output file named after the XenDesktop 7.x Site.
	
	Word and PDF Document includes a Cover Page, Table of Contents, and Footer.
	Includes support for the following language versions of Microsoft Word:
		Catalan
		Chinese
		Danish
		Dutch
		English
		Finnish
		French
		German
		Norwegian
		Portuguese
		Spanish
		Swedish

NOTE: This script requires PowerShell V3 or later.
NOTE: Best performance is obtained by using PowerShell V5.
NOTE: Word 2007 is not supported.
Support for non-English Versions of Microsoft Word
The script supports the following languages:
•	Catalan
•	Chinese
•	Danish
•	Dutch
•	English
•	Finnish
•	French
•	German
•	Norwegian
•	Portuguese
•	Spanish
•	Swedish
 
Prerequisites
Let us ensure we have the requirements before using PowerShell to document anything in a XenDesktop 7.x Site.
1.	If the script runs remotely, there are two choices: install Citrix Studio or manually install the PowerShell snapins.
a.	Install Studio from the full XenDesktop 7.x installation media. Installing Citrix Studio installs all the necessary PowerShell snapins.
b.	Install the PowerShell snapins individually. Depending on the bitness of the computer, from the full XenDesktop 7.x installation media, install the following files from either x64 or x86 (?? is either 86 or 64):
i.	Citrix Desktop Delivery Controller\ADIdentity_PowerShellSnapIn_x??
ii.	(Only for XenDesktop 7.6 and later) Citrix Desktop Delivery Controller\Analytics_PowerShell_SnapIn_x??
iii.	Citrix Desktop Delivery Controller\Broker_PowerShell_SnapIn_x??
iv.	Citrix Desktop Delivery Controller\Configuration_PowerShell_SnapIn_x??
v.	Citrix Desktop Delivery Controller\ConfigurationLogging_PowerShell_SnapIn_x??
vi.	Citrix Desktop Delivery Controller\DelegatedAdmin_PowerShellSnapIn_x??
vii.	Citrix Desktop Delivery Controller\EnvTest_PowerShell_SnapIn_x??
viii.	Citrix Desktop Delivery Controller\Host_PowerShell_SnapIn_x??
ix.	Citrix Desktop Delivery Controller\MachineCreation_PowerShellSnapIn_x??
x.	Citrix Desktop Delivery Controller\Monitor_PowerShellSnapIn_x??
xi.	Citrix Desktop Delivery Controller\Storefront_PowerShellSnapIn_x??
xii.	Citrix Policy\CitrixGroupPolicyManagement_x??
xiii.	DesktopStudio\PxAppV_Studio_PowershellSnapin_x??
xiv.	Licensing\LicensingAdmin_PowerShellSnapIn_x??

Script Usage
How to use this script?
1.	Save the script as XD7_Inventory.ps1 in your PowerShell scripts folder.
2.	From the PowerShell prompt, change to your PowerShell scripts folder.
3.	From the PowerShell prompt, type in:
a.	.\XD7_Inventory.ps1 and press Enter.
4.	By default, a Microsoft Word document is created named after the XenDesktop 7.x Site.
5.	If you use the –PDF option, a PDF file is created named after the XenDesktop 7.x Site.
6.	If you use the –HTML option, an HTML file is created named after the XenDesktop 7.x Site.
7.	If you use the –Text option, a Text file is created named after the XenDesktop 7.x Site.
To run the script against a remote Controller:
.\XD7_Inventory.ps1-AdminAddress DDCName and press Enter.
Full help text is available.
Get-Help .\XD7_Inventory.ps1 –full

The help text explains all the parameters the script accepts.
