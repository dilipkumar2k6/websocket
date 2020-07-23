# TCP
## TCP 3 way handshake 
![](assets/tcp-3-ways-handshake.png)
## TCP flow control
![](assets/tcp-flow-control.png)
## TCP data handshake, data transfer and closing connection
![](assets/tcp-full-flow.png)
# HTTP
- A higher layer protocol which sends data to TCP
# Web Socket
## Why?
- Need something for real time collaboration
- low latency
- 2 way push
- browser to server
## Details
- Websocket is inside the TCP socket
![](assets/websocket.png)
- After http handshake, it use `101` i.e. switching protocol 
![](assets/websocket-after-http.png)
    - Websocket was first to use `101`
    - After that same TCP connection turns into websocket
    - It also exchanges protocol version, sub protocol version, extension etc
    ![](assets/websocket-upgrade.png)
- Key accepts
![](assets/websocket-key-accept.png)
![](assets/websocket-key-accept-more.png)
![](assets/websocket-internet-full-of-cache.png)
- Version negotiations
![](assets/websocket-version-exchange.png)
- Sub protocol negotiations
![](assets/websocket-sub-protocol.png)
- Data exchange
![](assets/data-exchange.png)
    - Web socket is message based
    - Use javascript interface
    - Server can send message
    - Client can send message
    - Client message is always mask
    - Server message is never masked
    - It can sends binary/text data
    ![](assets/kind-of-messages.png)
    - Data is send as series of frames
    ![](assets/data-frames.png)
    ![](assets/whyframes.png)
 ## Node.js example
 ### Communication between client and server
 - How can we connect two clients for bidirectional messaging?
 - You have to do some routing in your server app which will act as brokers for two client. 
 - You can't always connect to two clients bcz they don't have always public accessible IP
 - Your server app will always have public ip
 - That's why server app is necessary if you want to implement peer to peer bidirectional 
 ![](assets/peer-to-peer.png)
 ### Communication between browser and server
 - socket programming in browser is bit complicated, but websocket is not
 - In browser, we can natively use the websocket protocol
### Communication between client to client 
- You can use pubnub service
![](assets/client-to-client.png)

# Reference 
https://www.youtube.com/watch?v=YaJbc7s1ROg
https://www.youtube.com/watch?v=9FqjRN4VYUU
