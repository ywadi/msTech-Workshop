# msTech-Workshop
The MS-Tech workshop, connecting arduino through MQTT to Azure IoTHub

## Setup IoT Hub 

### Create an IoT hub

Create an IoT hub for your simulated device app to connect to. The following steps show you how to complete this task by using the Azure portal.

1. Sign in to the Azure portal.

2. In the Jumpbar, click New > Internet of Things > IoT Hub.

![Azure Hub](https://docs.microsoft.com/en-us/azure/includes/media/iot-hub-get-started-create-hub/create-iot-hub1.png)

3. In the IoT hub blade, choose the configuration for your IoT hub.

![](https://docs.microsoft.com/en-us/azure/includes/media/iot-hub-get-started-create-hub/create-iot-hub2.png)

- In the Name box, enter a name for your IoT hub. If the Name is valid and available, a green check mark appears in the Name box.

- Select a pricing and scale tier. This tutorial does not require a specific tier. For this tutorial, use the free F1 tier.

- In Resource group, either create a resource group, or select an existing one. For more information, see Using resource groups to manage your Azure resources.

- In Location, select the location to host your IoT hub. For this tutorial, choose your nearest location.

4. When you have chosen your IoT hub configuration options, click Create. It can take a few minutes for Azure to create your IoT hub. To check the status, you can monitor the progress on the Startboard or in the Notifications panel.

![](https://docs.microsoft.com/en-us/azure/includes/media/iot-hub-get-started-create-hub/create-iot-hub3.png)

5. When the IoT hub has been created successfully, click the new tile for your IoT hub in the Azure portal to open the blade for the new IoT hub. Make a note of the Hostname, and then click Shared access policies.

![](https://docs.microsoft.com/en-us/azure/includes/media/iot-hub-get-started-create-hub/create-iot-hub4.png)

6. In the Shared access policies blade, click the iothubowner policy, and then copy and make note of the IoT Hub connection string in the iothubowner blade. For more information, see Access control in the "IoT Hub developer guide."

![Shared access policies blade](https://docs.microsoft.com/en-us/azure/includes/media/iot-hub-get-started-create-hub/create-iot-hub5.png)

You have now created your IoT hub.

## Registering a Device 

1. Instal the device explorer using NodeJS, to download nodejs please reffer to https://nodejs.org/en/download/package-manager/

2. Download the iothub-explorer CLI tool 
`npm install iothub-explorer`

3. Copy your connection string from the Zure portal 

![key](https://docs.microsoft.com/en-us/azure/includes/media/iot-hub-get-started-create-hub/create-iot-hub5.png)


4. Use the iothub-explorer tool to create a device and generate a sas token 

- Create Device `iothub-explorer create myArduino --login '{connection string}'`

- Create SaS Token `iothub-explorer sas-token myArduino --login {connection string}`

- Save your SaS token 'SharedAccessSignature sr=####&se=####'

### Install the Arduino IDE from the following link 

https://www.arduino.cc/en/main/software

http://www.instructables.com/id/Quick-Start-to-Nodemcu-ESP8266-on-Arduino-IDE/

