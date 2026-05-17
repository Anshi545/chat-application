# Chat Application

A simple Java Swing based chat application that demonstrates one-to-one messaging between a server window and a client window. The project uses Java sockets for communication and a WhatsApp-style Swing interface for sending and displaying messages with timestamps.

## Features

- Desktop chat UI built with Java Swing
- Separate `Server` and `Client` applications
- Socket-based message transfer using localhost
- Message bubbles with timestamps
- Profile, phone, video, back, and menu icons
- NetBeans Ant project structure

## Technologies Used

- Java
- Java Swing
- Java Socket Programming
- NetBeans IDE
- Apache Ant

## Project Structure

```text
src/
  chatting/application/
    Server.java
    Client.java
  icons/
    image and UI icon assets
nbproject/
  NetBeans project configuration
build.xml
manifest.mf
```

## Working Process

1. Run `Server.java` first.
2. The server creates a chat window and starts listening on port `6001`.
3. Run `Client.java` after the server is active.
4. The client connects to `127.0.0.1:6001`.
5. When a user types a message and clicks `Send`, the message is written to the socket using `DataOutputStream`.
6. The receiving side reads the message using `DataInputStream`.
7. Each message is shown in the chat panel with a timestamp.
8. The server and client continue listening for new messages until the application is closed.

## How to Run

### Using NetBeans

1. Open this project in NetBeans.
2. Run `src/chatting/application/Server.java`.
3. Run `src/chatting/application/Client.java`.
4. Start chatting between the two windows.

### Using Command Line

Compile the project:

```bash
javac -d build/classes src/chatting/application/*.java
```

Copy the `icons` folder into `build/classes` if needed, then run:

```bash
java -cp build/classes chatting.application.Server
java -cp build/classes chatting.application.Client
```

Run the server command first, then run the client command in a second terminal.

## Notes

- This project currently works on localhost.
- Start the server before starting the client.
- The default port is `6001`.
