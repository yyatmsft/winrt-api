---
-api-id: P:Windows.Networking.Sockets.IWebSocketControl.SupportedProtocols
-api-type: winrt property
---

<!-- Property syntax
public Windows.Foundation.Collections.IVector<string> SupportedProtocols { get; }
-->

# Windows.Networking.Sockets.IWebSocketControl.SupportedProtocols

## -description
Gets a collection that can be used to add a list of supported sub-protocols that will be advertised to the server during the connect handshake.

## -property-value
A collection that contains the WebSocket sub-protocols supported by the [IWebSocket](iwebsocket.md) object.

## -remarks
The [SupportedProtocols](iwebsocketcontrol_supportedprotocols.md) property contains a collection of WebSocket sub-protocols supported by the [IWebSocket](iwebsocket.md) object. Before calling the [ConnectAsync](iwebsocket_connectasync.md) method, additional supported sub-protocol strings can be added to this collection, which will be sent to the server in the "Sec-WebSocket-Protocol" header during the WebSocket handshake. The protocol chosen by the WebSocket server will then be exposed on the [Protocol](iwebsocketinformation_protocol.md) property.

An attempt to add a sub-protocol to this collection after a successful call to [ConnectAsync](iwebsocket_connectasync.md) method will result in an error. However, if the [ConnectAsync](iwebsocket_connectasync.md) method call or the connect operation completes with an error, an appl can update the collection stored in the [SupportedProtocols](iwebsocketcontrol_supportedprotocols.md) property and retry the [ConnectAsync](iwebsocket_connectasync.md) method call.

## -examples

## -see-also
[IWebSocket](iwebsocket.md), [IWebSocketInformation.Protocol](iwebsocketinformation_protocol.md), [How to use advanced WebSocket controls](http://msdn.microsoft.com/library/0a47f7c3-66f9-4315-886e-bd1afe77bf39)