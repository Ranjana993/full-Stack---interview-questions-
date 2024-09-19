# Nodejs interview questions from very basic to very advanced

# *Basic*

### Q1 . What is node.js?

- Node.js is neither a language nor a framework.
- Node / Node.js is a runtime environment for executive JavaScript code on the server side.

### Q2 . How is Node a runtime environment on the server side? what is V8?

- Browser executes JavaScript on the client side; similarly, Node.js executes JavaScript on the server side.
- V8 is a JavaScript engine for the JavaScript language.

### Q3 . What is the difference between Runtime environments & Framework?

- Run time environment: Primarily focuses on providing the necessary infrastructure for code execution, including services like memory management and I/O operation.
- Frameworks: These primarily focus on simplifying the development process by offering a structured set of tools, libraries, and best practices.

### Q4 . What is the difference between Node.js and express.js?

- Node.js is a runtime environment that allows the execution of JavaScript code on the server side .
- Express.js is a framework built on the top Node.js
    - it is designed to simplify the process by building web applications and APIs by providing a set of features like simple routing system, middleware support etc.

### Q5 . What is the difference between Client side ( Browser ) & Server side ( Node.js )?

## *Main Features of Node.js*

### Q1. What are the 7 main features of node.js?

1. Single-threaded
2. Asynchronous 
3. Event Driven
4. V8 JavaScript Engine 
5. Cross Platform
6. NPM (Node Package Manager )
7. Real-Time Capabilities 

### Q2. What is single-threaded programming?

**Single-threaded programming** refers to a programming model in which a single thread is responsible for executing all tasks or instructions, one after the other, in sequence.

### Q3. What is Synchronous programming?

In synchronous programming, each task is performed one after the other, and the program waits for each operation to complete before moving on to the next one.

Synchronous programming focus on the order of execution in a sequential manner, while single-threaded programming focuses on the single thread. 

### Q4. What is Multi-threaded programming?

**Multi-threaded programming** is a programming model where a process is divided into multiple threads that run concurrently. Each thread can execute a sequence of instructions independently and in parallel with other threads, allowing multiple tasks to be performed simultaneously.

### Q5. What is Asynchronous programming?

**Asynchronous programming** is a programming paradigm that allows tasks to be executed without blocking the main thread, enabling the system to handle multiple operations concurrently. In this model, a task is initiated, and while waiting for it to complete (e.g., fetching data from a database or making an API call), the program can continue executing other tasks instead of being blocked.

### Q6. What is the difference between Synchronous and Asynchronous programming?

Synchronous programming executes tasks one after the other, where each task waits for the previous one to complete before starting. This can cause delays if a task takes a long time (like fetching data). In contrast, asynchronous programming allows tasks to run independently and doesn't block the program from moving to the next task while waiting for another to finish (like fetching data or reading a file). This makes asynchronous code more efficient, especially when handling tasks that take time, as the program can continue working without waiting.

![asynce.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/034d6e13-4e25-43f9-bb9c-78d27af5e899/9104df75-2698-4c32-a3b9-47b563296cc3/asynce.png)

### Q7. What is Events Events Emitter, Event Queue, Event Loop and Event Driven?

- **Event**: An occurrence (like a button click or data received from a server) that triggers a response in the program.
- **Event Emitter**: An object that triggers (emits) events, which can be listened to and handled by other parts of the program.
- **Event Queue**: A queue where events and their corresponding callbacks are stored to be processed by the event loop.
- **Event Loop**: A mechanism that checks the event queue and ensures asynchronous callbacks are executed when the main thread is free.
- Event Handler: Function that respond to specific events.
- **Event-Driven Programming**: A programming model where the flow of the program is determined by events and their handlers. Node.js, for example, is designed around this model.

### Q8. What are the main features & advantages of node.js?

### **Main Features of Node.js**

1. **Asynchronous**:
    - Node.js operates asynchronously, meaning it can perform non-blocking I/O operations, allowing the execution of multiple tasks without waiting for any one of them to complete. This is especially useful in handling requests in web applications.
2. **Single-Threaded**:
    - Although Node.js uses a single thread to handle tasks, it leverages non-blocking I/O and asynchronous processing to manage a large number of connections concurrently, making it highly scalable.
3. **Fast Execution with V8 Engine**:
    - Node.js is built on the Chrome V8 JavaScript engine, which compiles JavaScript to native machine code, making it extremely fast for both server-side and client-side scripting.
4. **Cross-Platform**:
    - Node.js is cross-platform, which means it can run on various operating systems such as Windows, Linux, and macOS.
5. **NPM (Node Package Manager)**:
    - Node.js has a built-in package manager called NPM, which provides access to thousands of pre-built libraries and modules. This vast ecosystem helps developers to speed up development by reusing existing solutions.
6. **Event Loop and Non-blocking I/O**:
    - The event loop mechanism in Node.js ensures that I/O operations (like reading/writing to a database or file) do not block the execution of code. It uses callbacks to handle I/O tasks asynchronously.
7. **Stream API**:
    - Node.js supports stream-based processing, which means you can handle large amounts of data by processing it in chunks rather than loading everything into memory at once.
8. **Real-time Applications**:
    - Node.js is ideal for developing real-time applications like chat applications, live updates, online gaming, etc., due to its non-blocking and event-driven architecture.

---

### **Advantages of Node.js**

1. **High Performance**:
    - Node.js is known for its speed and efficiency in handling concurrent requests. This makes it perfect for applications that handle a lot of data or need to process requests quickly, such as real-time applications (chat apps, streaming services).
2. **Scalability**:
    - Due to its asynchronous, non-blocking architecture, Node.js is highly scalable. This makes it an excellent choice for building applications that need to handle a high volume of traffic or connections.
3. **Efficient for I/O-heavy Applications**:
    - Node.js is particularly well-suited for I/O-heavy applications, such as those that perform file operations, network requests, and database access. This allows for faster data handling compared to traditional server-side languages.
4. **Single Programming Language (JavaScript)**:
    - Node.js allows developers to use JavaScript for both client-side and server-side development. This unification reduces the need to switch between different programming languages and makes development faster.
5. **Active Community and Ecosystem**:
    - Node.js has a large and active open-source community, which continuously contributes to its ecosystem. The vast number of packages and libraries available through NPM significantly speeds up development.
6. **Real-time Applications**:
    - Node.js excels in building real-time applications like chat apps, online gaming, and collaborative tools. Its event-driven nature allows for fast communication between server and clients.
7. **Cost-Effective**:
    - With Node.js, a single programming language (JavaScript) is used across both client-side and server-side. This reduces the complexity of hiring developers and streamlines the development process, potentially lowering the cost of development.
8. **Memory Efficient**:
    - Since Node.js is event-driven and handles I/O asynchronously, it is highly memory-efficient, which is crucial for large-scale applications that need to handle high traffic without consuming excessive memory.
9. **Proxy Server Capabilities**:
    - Node.js can be used as a proxy server to handle a large number of concurrent connections and act as an intermediary for services with different response times.

### Q9. What are the disadvantages of nodejs?

# *Project setup and Modules*

### Q1 How do you set up node.js projects?

1. **Install Node.js**: Download and install Node.js from [nodejs.org](https://nodejs.org/).
2. **Create Project Directory**:
    
    ```jsx
    bash
    Copy code
    mkdir project-name
    cd project-name
    ```
    
3. **Initialize Project**:
    
    ```jsx
    bash
    Copy code
    npm init -y
    ```
    
4. **Install Dependencies**:
Install any required packages (e.g., Express.js):
    
    ```bash
    bash
    Copy code
    npm install express
    
    ```
    
5. **Create `index.js` File**:
Inside the project directory, create `index.js` as the main entry point.
6. **Set Up Basic Server** (for Express):
    
    ```jsx
    javascript
    Copy code
    const express = require('express');
    const app = express();
    
    app.get('/', (req, res) => {
      res.send('Hello, World!');
    });
    
    app.listen(3000, () => {
      console.log('Server is running on port 3000');
    });
    ```
    
7. **Run the Server**:
    
    ```jsx
    bash
    Copy code
    node index.js
    
    ```
    
8. **Add Scripts in `package.json`** (Optional):
    
    ```json
    json
    Copy code
    "scripts": {
      "start": "node index.js"
    }
    
    ```
    
9. **Use `nodemon` for Auto-Restart** (Optional):
Install `nodemon`:
    
    ```bash
    bash
    Copy code
    npm install --save-dev nodemon
    
    ```
    
    Update the start script:
    
    ```jsx
    json
    Copy code
    "scripts": {
      "start": "nodemon index.js"
    }
    
    ```
    
10. **Run the Project**:
    
    ```jsx
    bash
    Copy code
    npm start
    
    ```
    

This sets up a basic Node.js project that is ready for development.

### Q2.  What is NPM? What is the role of the node_modules folder?

- **NPM**: A package manager for JavaScript that helps install, manage, and share packages.
- **node_modules folder**: Stores all the project dependencies (packages and their sub-dependencies) installed by NPM for the project to use.

### Q3. What is the role of package.json file in Node.js?

The `package.json` file in Node.js manages project metadata, dependencies, scripts, and version control. It specifies essential information like the project name, version, dependencies, and custom commands, enabling easy project setup and maintenance.

### Q4.  What are Modules in Node?

**Modules** in Node.js are reusable blocks of code that can be exported and imported across different files in a Node.js project. They help organize code and promote modularity.

Type of module :

- Core module
- Local Module
- Third-Party Modules

### Q5.  How many ways are there to export a module?

In Node.js, there are two primary ways to export a module:

### 1. **Using `module. exports`**:

- This allows exporting a single value (object, function, class, etc.) from a module.

**Example**:

```jsx
// math.js
const add = (a, b) => a + b;
module.exports = add;
**Usage**:
```

```jsx
const add = require('./math');
console.log(add(2, 3)); // 5
```

### 2. **Using `exports`**:

- This is a shorthand to add multiple properties to the `module. exports` object.

**Example**:

```jsx
// math.js
exports.add = (a, b) => a + b;
exports.subtract = (a, b) => a - b;

```

**Usage**:

```jsx
const math = require('./math');
console.log(math.add(2, 3)); // 5
console.log(math.subtract(5, 2)); // 3

```

### Q7. What will happen if you don’t export the module?

If we don’t export a module in Node.js, the contents of that module will not be accessible to other files in the project. When you try to require a module that isn’t exported, it will return an empty object (`{}`) by default.

### Q8. How to import single and multiple functions from a module?

- For a **single function**, we use the `module. exports`.
- For **multiple functions**, we use `exports` and destructuring for cleaner imports.

### Q9. What is the module wrapper function?

The **module wrapper function** in Node.js is a hidden function that wraps every module in Node.js, providing module-level encapsulation and ensuring that variables and functions defined in one module do not pollute the global scope. How It Works:

When a module is loaded, Node.js wraps the entire code of the module inside the following function:

```jsx
(function (exports, require, module, __filename, __dirname) {
  // Module code actually lives here
});
```

# *Top built-in modules*

### Q1. What are the top 5 built-in modules commonly used in node projects?

The top 5 commonly used **built-in modules** in Node.js:

### 1. **`fs` (File System)**

- Used for interacting with the file system, such as reading, writing, and modifying files.
- Example:
    
    ```jsx
    const fs = require('fs');
    fs.readFile('example.txt', 'utf8', (err, data) => {
      if (err) throw err;
      console.log(data);
    });
    ```
    

### 2. HTTP

- Used for creating HTTP servers and handling requests/responses.
- Example:
    
    ```jsx
    const http = require('http');
    const server = http.createServer((req, res) => {
      res.statusCode = 200;
      res.setHeader('Content-Type', 'text/plain');
      res.end('Hello, World!\n');
    });
    server.listen(3000, () => {
      console.log('Server running on port 3000');
    });
    ```
    

### 3. **`path`**

- Provides utilities for handling and transforming file paths.
- Example:
    
    ```jsx
    const path = require('path');
    const filePath = path.join(__dirname, 'example.txt');
    console.log(filePath);
    ```
    

### 4. **`os`**

- Provides operating system-related utility methods and properties.
- Example:
    
    ```jsx
    const os = require('os');
    console.log('OS Platform:', os.platform());
    console.log('Total Memory:', os.totalmem()
    ```
    

### 5. **`events`**

- Allows creating and managing event-driven programming using custom events.
- Example:
    
    ```jsx
    const EventEmitter = require('events');
    const emitter = new EventEmitter();
    emitter.on('greet', () => {
      console.log('Hello there!');
    });
    emitter.emit('greet');
    
    ```
    

### Q2. Explain the role of the fs module. Name some function of it. ?

fs (File System ): The fs module in the node provides a set of methods for interacting with the file system. 

- **fs.readFile(**) ⇒ Read the content of the file specified.
- **fs.writeFile()** ⇒ Write data to the specified file, creating the file if it does not exist .
- **fs.appendFile()** ⇒ Append the data to a file. If the file does not exist, it is created .
- fs. readdir() ⇒ Reads the content of a directory.
- **fs. unlink()** ⇒ Delete the content of a directory .
- **fs.mkdir()** ⇒ Create a new directory .
- **fs.rmdir()** ⇒ remove the specified directory .

### Q3. Explain the role of the path module. Name some function of it ?

The path module provides utilities for joining, resolving, parsing formatting, normalizing and manipulating. 

### Q4. Explain the role of OS module. Name some functions of it.

### Q5. Explain the role of the events module. How to handle events in Node.js?

### Q6. What are the Event arguments?

### Q7. What is the difference between a function and an event?

### Q8. What is the role of the HTTP module in the node?

### Q9. What is the role createServer() method of the HTTP module?

# Express - Basics

### What are the advantage of using express.js with Node.js?

### How do you install express.js in a Node.js project ?

### How to create an HTTP Server using Express.js?

### How do you create and start an Express.js application?