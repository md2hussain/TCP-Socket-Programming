# TCP Socket Programming

This project demonstrates a simple **TCP server implemented in Node.js** using the `net` module. The server listens for incoming connections and logs messages it receives. The communication is done using **`ncat`** (Netcat), a simple networking tool.

## Project Setup

### Prerequisites

Make sure you have the following installed:

- [Node.js](https://nodejs.org/) (which includes npm)
- [ncat](https://nmap.org/ncat/)

### Installation

1. Clone the repository to your local machine:
   ```bash
   git clone https://github.com/md2hussain/TCP-Socket-Programming.git
   cd TCP-Socket-Programming
   ```

2. Install the necessary Node.js modules (if any):
   ```bash
   npm install
   ```

## Running the Project

### Start the TCP server:

In the project folder, run the following command to start the server:
```bash
node server.js
```

### Send messages using `ncat`:

Open a new terminal window and use **`ncat`** to connect to the TCP server:
```bash
ncat 127.0.0.1 5500
```
You can replace `127.0.0.1` with the IP address of the server and `5500` with the desired port if different.

Type your message and press **Enter** to send it.

### Server Logs:

The server will display the received message along with the sender's details.

## Example

1. **Run the server:**
   ```bash
   node server.js
   ```

2. **Connect and send a message from `ncat`:**
   ```bash
   ncat 127.0.0.1 5500
   ```
   Type:
   ```
   Hello from Netcat
   ```
   The server will output something like:
   ```bash
   Client connected from 127.0.0.1:xxxx
   Server received: Hello from Netcat
   ```

## Project Structure

```
TCP-Socket-Programming/
│
├── server.js           # The TCP server implementation
├── README.md           # Project documentation
├── .gitignore          # Git ignore file (to ignore node_modules, etc.)
└── package.json        # Node.js project configuration
```

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
