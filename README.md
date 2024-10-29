<!-- # [ zrfisaac ] -->

<!-- # [ about ] -->
<!-- # - author : Isaac Caires -->
<!-- # . - email : zrfisaac@gmail.com -->
<!-- # . - site : zrfisaac.github.io -->

<!-- # [ markdown ] -->
# Cromis IPC 1.6.1

- **Original Author:** Iztok Kacin
- **Current Maintainer:** Isaac Caires
- **License:** Freeware
- **Original Release Date:** February 20, 2014
- **Category:** Components > System > Apps Communications

## Overview

**Cromis IPC** (Inter-Process Communication) is a Delphi component designed to facilitate fast and efficient communication between applications using **Named Pipes**. This library abstracts away the technical complexities of IPC, providing a **client-server** communication model that is **thread-safe** and highly optimized for fast messaging.

## Key Features

- **Fast Communication:** Provides a highly efficient communication channel with an average message transmission time of 0.1 ms.
- **Packet-Oriented Messaging:** Data is sent in structured packets for easier handling.
- **Client-Server Architecture:** Allows multiple clients to communicate with a server in a multi-threaded, thread-safe environment.
- **Thread Pool Management:** Server side is multi-threaded, utilizing a thread pool for optimal resource management.
- **Versatile Data Packets:** Packets can carry different types of data, allowing flexible usage scenarios.
- **Fully Functional and Ready for Deployment:** The component is well-tested and reliable, with source code included.

## Compatibility

**Cromis IPC** is compatible with the following Delphi platforms:

- Delphi 2006
- Delphi 2007
- Delphi 2009
- Delphi 2010
- Delphi XE
- Delphi XE2
- Delphi XE3
- Delphi XE4
- Delphi XE5

## Installation

- **Download the Library:** Obtain the Cromis IPC source code compatible with your version of Delphi from the official download repository.
- **Add to Delphi Library Path:**
  - In Delphi, go to **Tools > Options > Delphi Options > Library**.
  - Add the directory containing the Cromis IPC source files to the Library Path.
- **Compile:** Open the project or package file in Delphi and compile the Cromis IPC units to ensure all dependencies are correctly resolved.
- **Integrate:** Add Cromis IPC units to your Delphi project as needed to enable inter-process communication.

## Usage Example

Below is a basic outline of setting up a server-client communication with Cromis IPC.

- **Create Server:**

```delphi
var
  IPCServer: TIPCServer;
begin
  IPCServer := TIPCServer.Create('MyServerPipe');
  IPCServer.OnExecute := ServerExecute;
end;
```

- **Create Client:**
```delphi
var
  IPCClient: TIPCClient;
begin
  IPCClient := TIPCClient.Create('MyServerPipe');
  IPCClient.SendMessage(...);  // Example of sending a message to the server
end;
```

- **Handle Data in Server:**
```delphi
procedure ServerExecute(const AMessage: IIPCMessage);
begin
  // Process received messages
end;
```

For full examples and details, refer to the source code documentation or sample projects provided with the library.

## Performance

The component achieves a messaging speed of approximately 0.1 ms per transaction (client -> server -> client), making it suitable for high-performance applications requiring rapid data exchanges.

## Additional Information

This repository is currently maintained by Isaac Caires, who started working from the last source available [Cromis IPC 1.6.1](https://torry.net/components/system/apps-communications/cromis-ipc) and will continue to provide updates and support.
