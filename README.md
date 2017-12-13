# node-files

node files is node promise based that provide  easy way dealing with files 


* open your directory and install *node-files* as dependency
```
npm i n-files
```
* import the module
```js
const nfs = require('n-files');
//or 
const {read} = require('n-files');
```
* example

```js
(async function x() {
        let file = await nfs.read('./LICENSE');
        // loop on every single line of the file 
        for (let line of file.lines())
            if(line.startsWith('Copyright')) 
                console.log(line); // Copyright (c) 2017 Hosam Elnabawy
        console.log(file.count); // 17
});

```