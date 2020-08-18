# Changelog

## To be released
- Added multicast support.
- Added multicast example.
- Modified `connect()`/`listen()` functions api to make them simpler.
  Before:
    ```rust
    network.connect("127.0.0.1:1234".parse().unwrap(), TransportProtocol::Tcp);
    ```
  Now:
    ```rust
    network.connect_tcp("127.0.0.1:1234");
    ```
- Removed `TransportProtocol`.
- Free all resources in the *distributed* example.
- Fixed sending by endpoints created by `UdpListener`.
- Fixed bug when sending by UDP in the *basic* example.
- Added a simple TCP example.

## Release 0.3.2
- Internal behavior changed: non-blocking TCP stream.
- Fixed some UDP issues.
- Internal thread names for debugging easily.
- Modified *distributed* example to use UDP instead of TCP in the participant connections.

## Release 0.3.1
- Fixed issue with the `TcpListener`.
  Sometimes a socket was not registered into the connection registry
  if several endpoints connect to a same listener at the same time.
- Added a distributed example based on a discovery server.
- Added traces to `network_adapter` module
- Removed `Cargo.lock` to the tracking files.

## Release 0.3.0
- Added `send_with_priority()` method to the `EventSender` in order to emulate a LIFO in some cases.
- Added Debug trait to `NetEvent`.
- Minor API changes.
- Fixed *hello_world_server* example.

## Release 0.2.0
- Fixed issue when a listener is interrupted by OS.
- Added log traces.
- Minor API changes.
- Clean code, rename modules.

## Release 0.1.0
- First release