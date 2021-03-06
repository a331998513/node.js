# Some codes
*Initial settings*
```
1. npm init  || npm init -y (skip questionaire)    // install pacakage json
2. npm i -g nodemon (global) || npm i -D nodemon (local | dev dependency)  // install node_modules (term: node package)
3. .gitignore node_modules // prevent node_modules to be uploaded to the github coz its large!
4. npm run dev // 'dev' can be customized, check package.json > 'scripts'
```

*local server creation*
```
const http = require('http');

const HOSTNAME = process.env.HOSTNAME || "localhost";
const PORT = process.env.PORT || 3000;

const server = http.createServer((request, response)=>{
    response.statusCode = 200;
    response.setHeader('content-type', 'text/plain');
    response.end('hey jay');
}) 
server.listen(PORT,HOSTNAME, ()=>{
    console.log(`server running at http://${HOSTNAME}:${PORT}/`)
})
```

*some methods*
```
const { readFile, readFileSync } = require('fs');
const { writeFile, writeFileSync } = require('fs');
const { appendFile } = require('fs)';
const { unlink } = require('fs');
const { rename } = require('fs');
```


*Some basic promsie & async code structure*
```
const fs = require('fs); //file system
const {readFile, readFileSync} = require('fs);

//regular promise way
fs.readFile('hi.txt', 'utf8', (err,data)=>{ 
    if(err){}; console.log(data)
})

//asynchronous
try{
    const data = readFileSync('hi.txt', 'utf8');
    console.log(data);
}   catch(err){
    console.log(err);
}
console.log('content ouside async here');
```

![image](https://user-images.githubusercontent.com/78078898/119902483-921eb000-bf47-11eb-9c35-c2e5aabd2aec.png)
