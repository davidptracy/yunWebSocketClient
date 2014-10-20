======= Arduino YUN and node ws ========

In-progress sketch of simple communication between Arduino Yun and a browser via remote server and websockets.

In this case, the Yun has a variable resistor (FSR) being read by A0 and a push button on digital 7 (input) with an LED from digital 13 (output). When the button is pressed, sensor values are sent to linux side via Bridge. Once this happens, the linux side of the Yun emits the sensor values to a remote server, that serves a website. 

To run this example, you will need node, node ws, and socket.io.
npm install node
npm install ws
npm install socket.io

To start the server: 'node wsServer.js'

The server is listening for ws messages on port 3000 and socket.io connections on 4000. 