## Backend Questions

1. 𝗡𝗼𝗱𝗲.𝗷𝘀 𝗙𝘂𝗻𝗱𝗮𝗺𝗲𝗻𝘁𝗮𝗹𝘀
    <details><summary> What is Node.js, and how does it work?</summary>
    Node.js is a runtime environment that allows developers to run JavaScript code outside of a web browser. It was created to enable server-side programming using JavaScript, which was traditionally used only on the client side (within browsers).

    Here’s how Node.js works:

    1. **JavaScript Runtime:** Node.js is built on the V8 JavaScript engine, which is also used by Google Chrome. The V8 engine compiles JavaScript to machine code, making it fast and efficient.

    2. **Non-blocking I/O:** One of Node.js's most powerful features is its non-blocking, event-driven architecture. It uses an asynchronous model, which means tasks like reading files, handling HTTP requests, or interacting with databases don't block the main execution thread. This allows Node.js to handle many tasks at the same time, making it highly efficient for I/O-heavy tasks.

    3. **Single-threaded with Event Loop:** Node.js operates on a single thread, which means it handles one task at a time. However, thanks to its event loop, it can manage multiple operations without waiting for one to finish before starting the next. The event loop delegates tasks to the appropriate system resources (e.g., file system or network), and once the task is complete, it returns the result to the application.

    4. **Modules:** Node.js has a rich set of modules (libraries of code) that developers can use to extend its functionality. The npm (Node Package Manager) is the largest repository of open-source libraries for Node.js.

    Key Uses of Node.js:
    - **Web servers:** Node.js can easily create web servers without relying on traditional web server software.
    - **Real-time applications:** Its event-driven nature makes it suitable for real-time applications like chat apps, online gaming, and collaborative tools.
    - **API Development:** Node.js is often used to build RESTful APIs for interacting with databases, servers, or external services.
    </details>
    <details><summary> Explain the event-driven, non-blocking I/O model in Node.js.</summary>ssss</details>
    <details><summary> What are the differences between Node.js and traditional web server models (like Apache or Nginx)?</summary>ssss</details>
    <details><summary> How does the V8 engine work in Node.js?</summary>ssss</details>
    <details><summary> Explain the purpose and use of npm (Node Package Manager).</summary>ssss</details>
2. 𝗔𝘀𝘆𝗻𝗰𝗵𝗿𝗼𝗻𝗼𝘂𝘀 𝗣𝗿𝗼𝗴𝗿𝗮𝗺𝗺𝗶𝗻𝗴
    <details><summary> How do you handle asynchronous code in Node.js?</summary>ssss</details>
    <details><summary> What are callbacks, and how do they work in Node.js?</summary>ssss</details>
    <details><summary> Explain Promises and how they improve asynchronous code handling.</summary>ssss</details>
    <details><summary> How does async/await work in Node.js?</summary>ssss</details>
    <details><summary> What is the "callback hell," and how can you avoid it?</summary>ssss</details>

3. 𝗘𝘃𝗲𝗻𝘁 𝗟𝗼𝗼𝗽
    <details><summary> Describe the Node.js event loop.</summary>ssss</details>
    <details><summary>How does the event loop manage asynchronous operations in Node.js?</summary>ssss</details>
    <details><summary> What are the phases of the event loop?</summary>ssss</details>
    <details><summary> How does the event loop affect performance in a Node.js application?</summary>ssss</details>
    
4. 𝗠𝗼𝗱𝘂𝗹𝗲𝘀 𝗮𝗻𝗱 𝗣𝗮𝗰𝗸𝗮𝗴𝗲𝘀
    <details><summary> What are Node.js modules, and how do you create them?</summary>ssss</details>
    <details><summary> Explain the difference between CommonJS and ES6 modules.</summary>ssss</details>
    <details><summary> How does the module caching mechanism work in Node.js?</summary>ssss</details>
    <details><summary> What are some commonly used Node.js built-in modules?</summary>ssss</details>
5. 𝗙𝗶𝗹𝗲 𝗦𝘆𝘀𝘁𝗲𝗺 𝗮𝗻𝗱 𝗦𝘁𝗿𝗲𝗮𝗺𝘀
    <details><summary> How do you handle file operations (read, write, delete) in Node.js?</summary>ssss</details>
    <details><summary> Explain the difference between synchronous and asynchronous file operations.</summary>ssss</details>
    <details><summary> What are streams in Node.js, and how do they work?</summary>ssss</details>
    <details><summary> How do you handle large files using streams in Node.js?</summary>ssss</details>