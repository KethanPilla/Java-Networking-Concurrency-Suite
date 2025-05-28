# Java Threading and Web Server Examples

This repository contains educational examples demonstrating Java threading concepts and basic web server implementation for CIS 476.

## 📁 Files Overview

### Core Threading Examples

- **`StockCar.java`** - A `Runnable` implementation that simulates a stock car race
- **`TaskThreadDemo.java`** - Demonstrates how to create and manage multiple threads

### Web Server Components

- **`WebServer.java`** - Basic single-threaded web server listening on port 80
- **`WebTask.java`** - `Runnable` task for handling individual client connections

## 🏁 StockCar Racing Demo

The `StockCar` class simulates a racing car that prints its progress through 10 iterations. Each car is identified by a number (like NASCAR numbers: 88, 24, 48).

### Example Output
```
88: 0
88: 1
88: 2
...
88: 9FINISHED
```

### Running the Demo

```bash
javac StockCar.java TaskThreadDemo.java
java TaskThreadDemo
```

**Note:** Currently only thread1 (car #88) runs since the other threads are commented out in `TaskThreadDemo.java`.

## 🌐 Web Server Example

The web server demonstrates basic socket programming and can be extended to handle multiple concurrent connections using the `WebTask` class.

### Features

- Listens on port 80 (requires admin privileges on most systems)
- Serves a simple HTML response: "Hello **CIS 476** from: *My Multi-Threaded Server*"
- Includes basic error handling

### Running the Web Server

```bash
javac WebServer.java WebTask.java
sudo java WebServer  # sudo required for port 80
```

Then visit `http://localhost` in your browser.

## 🧵 Threading Concepts Demonstrated

1. **Implementing Runnable Interface** - Both `StockCar` and `WebTask` implement `Runnable`
2. **Thread Creation and Management** - `TaskThreadDemo` shows proper thread instantiation
3. **Concurrent Execution** - Multiple threads can run simultaneously (when uncommented)
4. **Practical Application** - Web server threading for handling multiple client requests

## 🚀 Exercises and Extensions

### Threading Exercises
- Uncomment all three threads in `TaskThreadDemo.java` to see concurrent execution
- Add `Thread.sleep()` calls to better observe thread interleaving
- Experiment with thread priorities using `Thread.setPriority()`

### Web Server Extensions
- Modify `WebServer.java` to use `WebTask` for handling multiple concurrent connections
- Add proper HTTP headers to the response in `WebTask.java`
- Implement request routing for different URLs

## ⚠️ Important Notes

- **Port 80 Access**: Running the web server requires administrator privileges on most systems
- **Resource Management**: The current `WebServer.java` only accepts one connection before closing
- **Error Handling**: Basic error handling is implemented but could be expanded

## 🔧 Compilation and Execution

### Compile All Files
```bash
javac *.java
```

### Run Threading Demo
```bash
java TaskThreadDemo
```

### Run Web Server (requires sudo/admin)
```bash
sudo java WebServer
```

## 📚 Learning Objectives

This code demonstrates fundamental concepts in:
- Java threading and concurrency
- Socket programming and network communication
- Runnable interface implementation
- Basic web server architecture
- Multi-threaded server design patterns

---
