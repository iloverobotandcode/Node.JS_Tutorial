e# Table of contents
1. Set up the environment --> **VSCode** [https://code.visualstudio.com/]
2. Set up the language program --> **NODE.JS** [https://nodejs.org/en]
3. Run the first code <*Hello World!*>
4. More examples
5. Problems and solutions
6. ReferencesReferences
---
## Set up the environment
1. Go to website [VSCode]([url](https://code.visualstudio.com/))
2. Download the VSCode (suitable with your operation system: Windows, Linux, MAC)
---
## Set up the language program
1. Go to the website [JS]([url](https://nodejs.org/en))
2. Download the NODE.JS version (should be the latest one)
3. Check the NODE.JS installation on the cmd
   1. Open the CMD or Powershell
   2. Write this command line to check the version <**node -v**>
---
## Run the first code
1. Copy and paste this code to your programming environment
```js
// index.js
console.log("Hello, World!");
```
2. Run this command line on the terminal of VSCode
- Syntax: **node file_name**
- Example below: file_name is **index.js**
```
node index
```
3. Show "Hello World!" on the **local host browser** - instead of showing on the terminal as above
```
http = require('node:http');
listener = function (request, response) {
   // Send the HTTP header 
   // HTTP Status: 200 : OK
   // Content Type: text/html
   response.writeHead(200, {'Content-Type': 'text/html'});
  
   // Send the response body as "Hello World"
   response.end('<h2 style="text-align: center;">Hello World!</h2>');
};

server = http.createServer(listener);
server.listen(3000);

// Console will print the message

console.log('Server running at http://127.0.0.1:3000/');
```
- How can we know it run? -
  - Open the browser and paste this link <http://localhost:3000>

---
## More examples
### How can we print out the result 4 when import 2 parameters 1 + 3?
1. Solution: Using **function**
- Topic: With or without function?
<table>
  <tr>
    <th>With function</th>
    <th>Without function</th>
  </tr>
  <tr>
    <td>
      <pre><code>
const add = (a, b) => {
  return a + b;
};
const sum = add(1, 3);
console.log(sum);
      </code></pre>
    </td>
    <td>
      <pre><code>
console.log(1 + 3);
      </code></pre>
    </td>
  </tr>
</table>

2. Solution: Using **require**
- Topic: From <index.js> access to <add.js>?
<table>
  <tr>
    <th>index.js</th>
    <th>add.js</th>
  </tr>
  <tr>
    <td>
      <pre><code>
require("./add");
      </code></pre>
    </td>
    <td>
      <pre><code>
const add = (a, b) => {
  return a + b;
};
const sum = add(1, 3);
console.log(sum);
      </code></pre>
    </td>
  </tr>
</table>

3. Solution: Using **module.exports**
- Topic: Function -> Require -> Module.exports
<table>
  <tr>
    <th>index.js</th>
    <th>add.js</th>
  </tr>
  <tr>
    <td>
      <pre><code>
const add = require("./add");
console.log(add(1, 3));  
      </code></pre>
    </td>
    <td>
      <pre><code>
const add = (a, b) => {
  return a + b;
};
module.exports = add;
      </code></pre>
    </td>
  </tr>
</table>

4. Solution: Using **REPL**
- Open the terminal
- Write the equation <1 + 3> and wait
- The result will be shown  

5. Solution: Using **Class**
- Topic: Function -> Require -> Module.exports -> Class
<table>
  <tr>
    <th>index.js</th>
    <th>add.js</th>
  </tr>
  <tr>
    <td>
      <pre><code>
const Add = require("./add");
Add.setNum1(1);
Add.setNum2(3);
console.log(Add.sum_result());
      </code></pre>
    </td>
    <td>
      <pre><code>
class Add {
    constructor (number1, number2) {
        this.number1 = number1;
        this.number2 = number2;
    }
    setNum1(num) {
        this.number1 = num;
    }
    setNum2(num) {
        this.number2 = num;
    }
    sum_result() {
        return this.number1 + this.number2;
    }
}
module.exports = new Add;
      </code></pre>
    </td>
  </tr>
</table>

## References
- doc tutorial 1: https://www.tutorialspoint.com/nodejs/nodejs_npm.htm
