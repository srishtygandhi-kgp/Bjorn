# Bjorn -- Redis-Like Key-Value Store

This repository contains a simple implementation of a key-value store inspired by Redis, implemented in C++. It consists of two main components: a client and a server, facilitating communication via sockets. The client allows users to interact with the server by sending commands, while the server processes these commands and manages the key-value data store.

## Features

- **Client-Server Architecture**: The system follows a client-server model, enabling multiple clients to communicate with the server concurrently.
- **Key-Value Store**: The server maintains an in-memory key-value store, allowing users to perform operations such as `GET`, `SET`, and `DEL` on stored data.
- **Non-Blocking IO**: The server handles multiple client connections efficiently using non-blocking IO techniques.
- **Basic Command Parsing**: The server parses client commands to perform corresponding actions on the key-value store.
- **Error Handling**: The system includes error handling mechanisms to manage unexpected situations gracefully.

## Files

- `client.cpp`: Contains the client-side code for sending commands to the server.
- `server.cpp`: Contains the server-side code for processing client commands and managing the key-value store.

## Usage

To use this Redis-like key-value store:

1. **Compile Code**: Compile the client and server code separately using a C++ compiler.
   
2. **Start Server**: Run the compiled server executable to start the server.

    ```bash
    ./server
    ```

3. **Interact with Client**: Use the client executable to send commands to the server. For example:

    ```bash
    ./client SET mykey myvalue
    ./client GET mykey
    ```

    Replace `mykey` and `myvalue` with your desired key and value.

4. **Check Server Response**: Observe the server's responses to your commands, including any errors or successful operations.

## Dependencies

This project relies on standard C++ libraries and does not have any external dependencies.

## Future Improvements

- **Persistence**: Implement data persistence mechanisms to store data persistently beyond the runtime of the server.
- **Advanced Data Structures**: Extend the key-value store to support more complex data structures like lists, sets, and sorted sets.
- **Security Measures**: Add authentication and access control features to enhance security.
