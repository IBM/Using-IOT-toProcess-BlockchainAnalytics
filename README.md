# Using-IOT-toProcess-BlockchainAnalytics

![](docs/iot-blockchain.png)


## Introduction
IoT's role in this project will take the users from the Blockchain network and list them as devices on the Watson IoT Platform everytime there's a new user created.

Besides that IoT will simulate a demo device and/or a real device can be chosen to display their data on the platform's dashboard. All these devices in this project will one Device Type.


![](docs/iot-dash.png)


That's with the Watson IoT Platform, but within Node-Red our IoT app will run analytics to display the total steps and total fitcoins of all users.

The app will also use a graph in real-time to show the Blockchain transactions coming to the IoT whether for new user creation, user validation or for generated values of steps and fitcoins.


![](docs/node-red-dash.png)


## Prerequisites
You will need the following accounts and tools:
* [IBM Cloud account](https://console.ng.bluemix.net/registration/)


## Steps of use
Choose from IBM Cloud/Bluemix Catalog the Internet of Things service, name it and create it. After few minutes when your app is ready, open Cloudant and create a database with the name of `secretmap` as seen below in the pic.


![](docs/cloudant.png)


Click your app's URL to open your Node-Red editor. Copy in there all the contents from the json file inside the scripts folder and paste them in the import box.

Blockchain Network will pass the blocks where all the information will be taken and be saved to be used for analytics and display the values on the Node-Red dashboard as seen in the above image.

* Make sure to have Cloudant database service available and binded to your Bluemix/IBM Cloud app instance.

* Make sure also to have a Watson IoT Platform created and binded as a service too.


![](docs/connections.png)


* Dashboard needs to be created in the Node-Red if it's not taken care of by the code import.


![](docs/nr-dash-setup.png)


* This is how the Node-Red code looks like:


![](docs/nodered-nodes.png)


* Watson IoT Platform list of devices preview:


![](docs/iot-platform.png)


* Values are passed in as json into: `'https://<YOUR-APP-NAME>.mybluemix.net/steps?message=' + blocks`


**Try live demo url:**
> [Demo display](https://think-iot-processor.mybluemix.net/ui/#/0)


## Useful links

* [IBM Cloud](https://bluemix.net/)  
* [IBM Cloud Documentation](https://www.ng.bluemix.net/docs/)  
* [IBM Cloud Developers Community](http://developer.ibm.com/bluemix)  
* [IBM Watson Internet of Things](http://www.ibm.com/internet-of-things/)  
* [IBM Watson IoT Platform](http://www.ibm.com/internet-of-things/iot-solutions/watson-iot-platform/)   
* [IBM Watson IoT Platform Developers Community](https://developer.ibm.com/iotplatform/)
* [Node Red](https://nodered.org/)


## License
[Apache 2.0](LICENSE)
