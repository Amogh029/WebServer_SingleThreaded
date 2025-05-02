# WebServer_SingleThreaded
Single Threaded Webserver using Java

# SingleThreaded Java Webserver Example

This project demonstrates a **simple single-threaded server and client** in Java. The server listens for incoming connections on a specified port, accepts one client at a time, and sends a greeting message. The client connects to the server, sends a message, and prints the server's response.

---

## Files

- `Server.java`  
  Implements a basic single-threaded server that listens on port 8010.

- `Client.java`  
  Implements a client that connects to the server, sends a message, and prints the response.

---

## How It Works

1. **Server**  
   - Listens on port `8010`.
   - Accepts one client connection at a time.
   - Sends `"Hello from server"` to the client.
   - Closes the connection.

2. **Client**  
   - Connects to `localhost:8010`.
   - Sends `"Hello from client"` to the server.
   - Reads and prints the server's response.

---

## How to Run

### 1. Compile

Open a terminal in the `SingleThreaded` directory and run:

```powershell
javac -d . Server.java
javac -d . Client.java
```

### 2. Start the Server

```powershell
java SingleThreaded.Server
```
You should see:
```
server is running on port 8010
```

### 3. Start the Client (in a new terminal)

```powershell
java SingleThreaded.Client
```
You should see:
```
Response from the socket is :Hello from server
```

---

## Notes

- Make sure the server is running **before** starting the client.
- Both files must have the `package SingleThreaded;` declaration at the top.
- The server handles one client at a time (single-threaded).
- If you get a `Connection refused` error, ensure the server is running and listening on the correct port.

---

