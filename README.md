# iOS ZMS Documentation

This documentation helps import and initialisation of ZMS iOS SDK. 


## Install  Prerequisites
- Minimum iOS version : iOS 12
- Cocoapods must to be installed : [Install Cocoapods](https://cocoapods.org)
- Minimum swift version : Swift 5
## Installation
Simply add the following line to your Podfile and install the pod.

```pod 'testSDK24', '1.2.1'  ```
Note: Name of pod and version will be updated once published.

## Usage Prerequisites

- Open the XCWorkspace notice that the dependency ZMS is now available.
- Go to the project settings -> Signing and Capabilities -> Enable background mode if it isn't already -> Check the location updates checkmark.
- Go to the info.plist file in project settings and add these 3 permissions with the appropriate descriptions to the users as to why permissions are used : 
		- Privacy - Motion Usage Description
		- Privacy - Location Always and When In Use Usage Description
		- Privacy - Location When In Use Usage Description
## Usage

First import the dependency by : 

```import ZMS```

Then, configure the SDK by providing a valid merchant token and signed JWT user token : 

```ZmsSdkManager.shared.configure(merchantId: "<MERCHANT_ID>", userToken: "<SIGNED_JWT_USER_TOKEN>")```

Then initialise the SDK Flow by calling the method : 
	 
	 ZmsSdkManager.shared.initilizeSDK(viewController: UIViewController, completion: {
		error in
		if let error = error {
			// handle error
		}
	// flow will start if there are no errors
	})

The viewController instance is used to show our flow, please make sure a navigation controller is initialised and the passed view controller instance is embedded in its navigation stack. 

## Please note

This document is subject to changes, as the whole process of publishing is not completed although the flow and processes should not change.


