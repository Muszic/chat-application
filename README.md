# Chat Application (Server-Client Model)
## Introduction
This project is a simple chat application that demonstrates a server-client model using C++ with sockets and threads. The server can handle multiple clients, allowing them to connect and communicate with each other. The server manages client connections, broadcasts messages, and handles disconnections gracefully. The client connects to the server and allows users to send and receive messages.

## Features
* Multiple clients can connect to the server simultaneously.
* Messages sent by a client are broadcasted to all other connected clients.
* Pending connection requests are managed using a queue.
* Disconnections are handled gracefully, and pending connections are processed.

## Technologies Used
* _C++:_ The primary programming language used for implementing the server and client.
* _Winsock API:_ Used for socket programming to manage network communications.
* _Multithreading:_ Used in the client code to handle message sending and receiving concurrently.

## Important Notes
1. _Environment:_ This project is designed to run on Windows, using the Winsock API for socket programming. Ensure you have the Windows SDK installed.
2. _Development Tools:_ Use Visual Studio for compiling and running the code. Visual Studio provides the necessary environment for compiling Winsock applications.
3. _Pending Connections:_ The server maintains a queue of pending connections when the maximum client limit is reached. Once a client disconnects, a pending connection is processed.
4. _Graceful Disconnection:_ Both server and client handle disconnections gracefully, ensuring resources are cleaned up properly.
5. _Linker Settings:_ Make sure to add wsock32.lib in the Project Properties -> Linker -> Input section. This is necessary for the code to work properly.

## Project Structure
* _Server Code:_ Manages client connections, receives and broadcasts messages.
* _Client Code:_ Connects to the server, sends messages, and receives from other clients.


## Server Code
The server code initializes Winsock, creates a socket, binds it to a port, and listens for incoming connections. It uses a select call to handle multiple client connections and broadcasts messages received from any client to all other connected clients.

## Client Code
The client code connects to the server, sends messages typed by the user, and receives broadcasts from the server. It uses a separate thread for receiving messages to allow simultaneous sending and receiving of messages.

## How To Run
1. _Server:_
* Open the server code in Visual Studio.
* Compile and run the server code.
* The server will start listening on port 9909.

2. _Client:_
* Open the client code in Visual Studio.
* Compile and run the client code.
* Connect to the server by running multiple instances of the client code.

## Example Usage
1. Start the server.
2. Run multiple instances of the client code.
3. Type messages in any client instance and see the messages broadcasted to all other connected clients.

## Future Enhancements
* _File Transfer:_ Working to add file transfer ability to the chat application for sharing files between clients.

## Conclusions
This project demonstrates a basic chat application using sockets and threads in C++. It serves as a foundational example for understanding server-client communication, handling multiple connections, and managing message broadcasting.

For further enhancements, consider adding features such as user authentication, encryption for secure communication, and a graphical user interface.

Feel free to explore the code and modify it to suit your needs!

*Note:* Please run these codes using Visual Studio and not Visual Studio Code.

## 🚀 About Me
My name is Sangeet, and I am currently pursuing BTech in Computer Science and Engineering from IIT Jammu. This project is part of my ongoing efforts to explore and understand network programming and concurrent processing using C++.

## 🔗 Links
[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/sangeet-sangwan-090196258/)