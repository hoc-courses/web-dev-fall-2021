# JavaScript Runtime Environment



While there is a single **specification **for the rules of a language, such as the supported data types and syntax, there are different **implementations **for how the code goes from the text you write in the code editor, to the machine instructions executing on a target computer. 

JavaScript is a somewhat unique in its implementation: how/when the JavaScript code is prepared for execution. Because JavaScript was designed specifically to run within a web browser, and the goal was to treat a JavaScript file similarly to other files included in a web page (images, fonts, stylesheets), the JavaScript code remains as text all the way to the time when the web browser reads it as it is loading the web page.

This means that there needs to be a component within the web browser that reads and interprets the instructions in the JavaScript code. That component is called the JavaScript Engine.

The JavaScript Engine is a separate entity from the web browser. The web browser delegates responsibility for executing JavaScript code to the JavaScript Engine.

Each web browser decides which JavaScript Engine to rely on for executing JavaScript code. In the Chrome browser, the JavaScript Engine is called V8, and is developed by Google. 

### Source Code to Machine Instructions

To understand why the JavaScript Engine is required to execute the JavaScript code, it is helpful to understand more broadly how a computer program, starting as text your write in a code editor, is translated into machine instructions that execute on the target computer.

Programming language implementations fall into a three broad categories depicted below.

![](<../.gitbook/assets/image (90).png>)

**Fully Compiled to Machine Code** - Lower-level languages like C/C++ are compiled to machine instructions prior to running on the target computer. The compiled code is only compatible with the matching computer architecture that understands the machine instruction set. Therefore, it is necessary to perform separate compilations for each target computer architecture.  Software applications, such as your web browser, fall into this category. When you go to the site to download the browser, you are asked to select the correct version to download based on the computer architecture it will run on. While program in this category have better performance, they are harder to produce, due to the added complexity of building/compiling for all the different computer architectures.

**Partially Compiled to Byte Code** - There is a set of languages (Java/C# are two examples) that are compiled into an intermediate form that is a machine-independent set of instructions. The advantage of this approach is that the machine-independent instructions can run on any target machine, but it requires a special machine-dependent application (called a virtual machine) to be running on the target computer to load the program and then further compile the machine-independent instructions into machine-dependent instructions. 

**Compilation is Deferred Until Code Execution **- This is the case for the JavaScript language. When a web page includes JavaScript code, either as a URL to an external file, or embedded within the`<script>`element , the web browser takes that JavaScript code (which is text) and passes it to the JavaScript Engine to interpret and execute the instructions in the code. 

In the early days of JavaScript, the JavaScript Engine just read each instruction, line by line, and interpreted each instruction and executed it  within its own application code. Now, the JavaScript Engine is very sophisticated and after initially reading and executing the JavaScript source code, it is able to optimize the code and compile it into machine instructions.

### JavaScript Runtime Environment

The image below depicts the JavaScript Runtime environment when code is run within a web browser. The web browser and the JavaScript Engine are two separate entities and the web browser relies on the JavaScript Engine to execute the JavaScript code.

![](<../.gitbook/assets/image (99).png>)

As we learned earlier, JavaScript now can also run outside of a web browser. Specifically, it can run in the JavaScript Runtime environment provided by the Node.js application and is often used to build web servers.

It is interesting to compare these two environments. In most ways they are very similar. They both have a component that loads the JavaScript code: the web browser or Node.js and both of these delegate executing the JavaScript code to the JavaScript Engine (Node.js also uses Google's V8 Engine).

But there are some difference, specifically the libraries of built-in objects that the environment provides. Within a web browser, the libraries include objects for accessing the browser window, and it's associated objects (document, history, location, console). Within Node.js, these objects are not included, because Node.js is not a web browser and those objects do not apply to JavaScript code running within Node.js. But there are additional built-in objects that are relevant to the Node.js environment, such as objects for loading files, which is not something that is supported within the browser environment.

![](<../.gitbook/assets/image (101).png>)
