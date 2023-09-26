# Analytics Web Widget

This is a Webex Device Web Widget which displays the local devices Room Analytics Data on the main display

![download (11)](https://github.com/wxsd-sales/analytics-web-widget/assets/21026209/2dda89e0-8858-4095-913e-c527e3009b9a)


## Overview

This Web Widget connects to the local device using a WebSocket and displays the devices Room Analytics data on the devices main display.

The Widget itself is a simple HTML and JavaScript file which uses the JSXAPI library to establish the WebSocket connection, initially reads the sensor values and the subscribes to them for changes.

More information on the JSXAPI library here: https://github.com/cisco-ce/jsxapi

In order for the Widget to open the WebSocket connection, it requires local account credentials for that device which are passed to the Widget in URL parameters.

As the connection to the device is local and not over Cloud xAPI. This Widget will work on Webex Devices registered in both Shared and Personal modes.


## Setup

### Prerequisites & Dependencies: 

- This Web Widget has been built only for the Webex Desk Series 
- RoomOS 11.8 or greater
- Web admin access to the device to upload the macro.
- (optional): Web Server to host your own copy of this Widget for customisation


<!-- GETTING STARTED -->

### Installation Steps:
1.  Log into your Webex Devices web interface
2.  Set WebEngine Mode to ```On``` and AllowDeviceCertificate to ```True```

![image](https://github.com/wxsd-sales/analytics-web-widget/assets/21026209/45b2af0b-31c7-4fd4-8086-f1e57dd1d3f1)


3.  Create a local account on the device with ```user``` and ```integrator``` roles and disable the password reset requirement. Note the username and password for the next step

![image](https://github.com/wxsd-sales/analytics-web-widget/assets/21026209/ba0c466a-e0d1-4f00-93ac-1bf44688a493)

4. Create a Web Widget using the UI Extension page and enter the URL for the Web Widget and include the username and password within the URL Parameters.
```
https://wxsd-sales.github.io/analytics-web-widget/widget.html?username=webwidget&password=Cisco123
```

![image](https://github.com/wxsd-sales/analytics-web-widget/assets/21026209/29cdc8d8-ace4-4f39-9b65-b531cb8ef7f8)


![image](https://github.com/wxsd-sales/analytics-web-widget/assets/21026209/69b6426b-b37e-42f0-ad07-cebd0579d028)


5. Upload the new Web Widget to the device by clicking on the blue upload icon

![image](https://github.com/wxsd-sales/analytics-web-widget/assets/21026209/dd615b03-df97-4830-a7e7-dbade263eb45)



    
## Validation

Validated Hardware:

* Desk Pro

This Web Widget should work on other Webex Devices but has not been validated at this time.
    
## Demo

*For more demos & PoCs like this, check out our [Webex Labs site](https://collabtoolbox.cisco.com/webex-labs).


## License

All contents are licensed under the MIT license. Please see [license](LICENSE) for details.


## Disclaimer
 
Everything included is for demo and Proof of Concept purposes only. Use of the site is solely at your own risk. This site may contain links to third party content, which we do not warrant, endorse, or assume liability for. These demos are for Cisco Webex use cases, but are not Official Cisco Webex Branded demos.


## Questions
Please contact the WXSD team at [wxsd@external.cisco.com](mailto:wxsd@external.cisco.com?subject=analytics-web-widget) for questions. Or, if you're a Cisco internal employee, reach out to us on the Webex App via our bot (globalexpert@webex.bot). In the "Engagement Type" field, choose the "API/SDK Proof of Concept Integration Development" option to make sure you reach our team. 
