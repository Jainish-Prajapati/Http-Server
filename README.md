# Http-Server

This repository contains implementations of a simple HTTP server in Java with three different concurrency models: SingleThreaded, MultiThreaded, and ThreadPool.

## Directory Structure

- `MultiThreaded`
  - `Server.java`
  - `Client.java`
- `SingleThreaded`
  - `Server.java`
  - `Client.java`
- `ThreadPool`
  - `Server.java`

## Concurrency Models

This project demonstrates three different approaches to handling multiple client requests concurrently in a server:

1. **SingleThreaded**:  
   In the single-threaded model, the server processes one client request at a time. This is simple to implement but can only handle one request concurrently, making it less suitable for real-time or high-traffic applications.

2. **MultiThreaded**:  
   In the multi-threaded model, the server creates a new thread for each client request. This allows multiple clients to be served simultaneously, providing better concurrency than the single-threaded model. However, creating a new thread for each request can become inefficient and resource-intensive under heavy load.

3. **ThreadPool**:  
   In the thread pool model, the server maintains a fixed number of reusable threads in a pool. When a client request is received, it is assigned to an available thread from the pool. This approach is more efficient than spawning new threads for each request, especially for applications with fluctuating or high request volumes, as it controls the number of active threads.



## Prerequisites

Ensure you have Java Development Kit (JDK) version 17 installed. If not, install it using the following commands:

For debian based distros
```bash
sudo apt-get update
sudo apt-get install openjdk-17-jdk
```

For Arch
```bash
sudo pacman -Syu
sudo pacman -S jdk21-openjdk
```
## Clone Repository

To clone this repository, open your terminal and run:

```bash
git clone https://github.com/Jainish-Prajapati/Http-Server.git
cd Http-Server
```

## Running the Servers and Clients

Each concurrency model has its own directory with server and client files. Follow these steps to compile and run the code for each model.

Eg. of Multithreaded

```bash
/*navigate to directory*/
cd MultiThreaded
/*Compile files*/
javac Server.java
javac Client.java
```

and similarly you can compile and run single threaded and threadpool servers too.

It's just an implementation of simple http server, developed to understand exactly how servers works internally irl !!  
