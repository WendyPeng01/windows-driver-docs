# FAQ on custom capabilities

## How are custom capabilities different from other capabilities?

1)  3rd party Microsoft partners can define new capabilities.

2)  They don't have to be built-in to Windows at compile time.

3)  App authorization to use the capability verifies during the app
    installation instead of when uploaded to the store.

## What’s the difference between UWP’s with Custom Capabilities and DCA’s (Device Companion Apps)?

|                           | **DCA**                                                  |  **RPAL**                                                   | **UWP App with Custom Capabilities**|
|---------------------------|----------------------------------------------------------|-------------------------------------------------------------|-------------------------------------|
|Communication|Device Scenario APIS (image capture, scanning, etc.)<br>Device protocol APIs (USB, HID, etc.)<br>Customer driver access|  Blanket access to APIS, Drivers, Services|DCA support + NT Services            |                                                                              
|Trust Model|Defined at a “container” level<br>The system's OEM must submit apps for internal components|Defined at a system level<br>The system's OEM must submit apps for internal components|Defined at a component level<br>IHVs own the trust boundaries for their components|
|Automatic App Acquisition  |Available for peripherals                                  | Not available                                               |Available for all hardware          |
|Deployment Dependencies    |WU: Driver package<br>Store: App|N/A – preload only|WU: Driver package<br>Store: App                  |
                                                                                                                                                    
                                                                                                            
                                                                                                                                                    
                                                  

For more information on DCA’s, see [Getting started with Windows Store
device
apps](https://msdn.microsoft.com/windows/hardware/drivers/devapps/getting-started).

