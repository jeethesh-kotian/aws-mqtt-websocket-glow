# aws-mqtt-websocket-glow

## Connecting esp8266 to AWS IoT to get thing's shadow json

ESP8266 is a highly integrated chip designed to connect to all the new world IoT devices and technology using Wifi network.
But ESP8266 do not support direct connection to AWS IoT due to lack of TLS 1.2 support.

So, the workaround is to connect to AWS IoT MQTT topics by using Web Socket at the Network Layer.

The file aws-mqtt-websocket-glow.ino above is an upgrade of the https://github.com/odelot/aws-mqtt-websockets/blob/master/examples/aws-mqtt-websocket-example/aws-mqtt-websocket-example.ino.
This will help to subscribe to specific AWS IoT topics and get feeds from the shadows. Also use the gpio2 pin of esp8266 as an output pin. 

## Note

AWSClient2.h is not mature and gives out compilation error, instead used the below AWSClient.
 ```
#include "AWSClient.h"
 ```

## Dependencies

| Library                   | Link                                                            | Use                 |
|---------------------------|-----------------------------------------------------------------|---------------------|
|aws-mqtt-websockets            |https://github.com/odelot/aws-mqtt-websockets                    |aws iot websocket example |
|aws-sdk-arduino*            |https://github.com/svdgraaf/aws-sdk-arduino                      |aws signing functions|
|arduinoWebSockets          |https://github.com/Links2004/arduinoWebSockets                   |websocket comm impl  |
|Paho MQTT for Arduino      |https://projects.eclipse.org/projects/technology.paho/downloads  |mqtt comm impl       |

## Reference and Tutorial

https://youtu.be/doqLJIQagJY



