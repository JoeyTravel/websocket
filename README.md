# websockets

 * [Bringing Sockets to the Web](https://www.html5rocks.com/en/tutorials/websockets/basics/)

 * ws: - URL schema for WebSocket connections
 * wss: secure WebSocket connections
 
 #
 
 Attaching event handlers immediately to the connection allows you to know when the connection is opened, received incoming messages, or there is an error.
 
 The second argument accepts optional subprotocols.  It can be a string or an array of strings.  Each string should represent a subprotocol name and server accepts only one of passed subprotocols in the array.  Accepted protocol can be determined bu accessing protocol property of WebSocket object.
 
    `//Object allows you to make client connections to a WebSocket server.`
    ``var WebSocketClient = require('websocket').client``

 # 
 
      // When the connection is open, send some data to the server
      connection.onopen = function () {
         connetion.send('Ping'); // Send the message 'Ping' to the server
      };
      
      // Log errors
      connection.onerror = function (error) {
         console.log('WebSocket Error ' + error);
      };
      
      // Log messages from the server
      connection.onmessage = function (e) {
         console.log('Server: ' + e.data);
      };
