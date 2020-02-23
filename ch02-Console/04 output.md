
# 04 Output  

## 输出控制

1. ### Style输出到控制台

``` javascript
console.log("%c NPM %c v6.2.0 ", "background:#555;color:white", "background:orange");
```


2. ### 使用{}包含输出变量
``` javascript
var name = "John";
var age = 20;
var size = 40;

console.log(name, age, size);  // John 20 40
console.log({name, age, size}); // {name: "John", age: 20, size: 40}
```
