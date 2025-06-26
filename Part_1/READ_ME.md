# Table of contents
1. Set up the environment --> **VSCode** [https://code.visualstudio.com/]
2. Set up the language program --> **NODE.JS** [https://nodejs.org/en]
3. Run the first code <*Hello World!*>
4. More examples
5. Problems and solutions
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
---
## More examples
1. Example: Build a code with function or without function
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

2. Example: From <index.js> access to <add.js>?
<table>
  <tr>
    <th>index.js</th>
    <th>add.js</th>
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
require("./add");
      </code></pre>
    </td>
  </tr>
</table>

