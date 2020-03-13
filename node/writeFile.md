## how to write object into file
```
let obj = {id: 1}
let str = JSON.stringfy(obj)
fs.writeFile(path, str, options)
```
