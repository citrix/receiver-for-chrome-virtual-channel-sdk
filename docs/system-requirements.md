# System requirements




## Execution Environment Requirements


* New data streams (audio and video)
* New devices, such as scanners, card readers, and joysticks

### Virtual Channel Overview




![](./virtual-channel-client-server-connection.png)

Citrix Receiver for Chrome Virtual Channel SDK is responsible for de-multiplexing the virtual channel data from the ICA data stream and routing it to the correct callback of the registered virtual channel. It is also responsible for sending the data using the appropriate object to the server in coordination with the Citrix Receiver for Chrome. Citrix Receiver for Chrome does not know any data package detail for each virtual channel and it only transfers all available data between the server and the client virtual driver.

	4. If the server application has data to send to the client, the data is sent to the client immediately. When the client receives the data, Citrix Receiver for Chrome de-multiplexes the virtual channel data from the ICA stream and passes to the third-party Chrome app implementing the virtual channel. Virtual Channel SDK routes the data to the appropriate callback of the registered object for that Virtual channel.
	5. If the client virtual driver has data to send to the server, the data is also sent immediately.



For example, if 100 bytes are sent to the server, the same 100 bytes are received by the server when the virtual channel is demultiplexed from the ICA data stream. The compiled code runs independently of the currently configured transport protocol.



1.	On a session launch, using the configuration the app ids and the stream names are fetched. This is used by the session for binding the Virtual Channel between the third-party Chrome app and Citrix Receiver for Chrome session.
* For details on signature and usage of APIs, see the [Programming Guide](./programming-guide.md). 

### Virtual Channel Packets
