
# 01 Global

## 全局函数

### 1.$  
类似于querySelector

``` javascript
// 选择文档中第一个div标签
document.querySelector('div')
$('div')
```

### 2.$$
类似于querySelectorAll但返回值是数组，不是NodeList

``` javascript
Array.from(document.querySelectorAll('div'))
$$('div')
```

### 3.$_
上一次执行结果的引用

``` javascript
(() => 123)() // 123
$_    // 123
```

### 4.$0
当前选中的节点，在console下试试  
依次类推，$1 $2 $3 $4分别是上一次选中的、上上一次、上上上一次、...  
PS: 
没有$5  
查看返回节点属性使用dir($0)  


### 5.copy

``` javascript
var person = {
    name: "John",
    age: 23,
}
copy(person);

// and then try to past in vscode
```

### 6.queryObjects  
查询类对应的实例

``` javascript
class Person {
    constructor(name, age) {
        this.name = name;
        this.age = age;
    }
}
const p1 = new Person("A", 10);
const p2 = new Person("B", 20);

queryObjects(Person);
```

### 7.monitor   
监控方法是否被调用（节省打console.log）  

``` javascript
class Person {
    constructor(name, age) {
        this.name = name;
        this.age = age;
    }
    
    getName() {
        return this.name;
    }
}
const p1 = new Person("A", 10);
const p2 = new Person("B", 20);

monitor(p1.getName)

p1.getName(); // function getName called
p2.getName(); // function getName called
```

### 8.monitorEvents    

``` javascript 
// Choose a node and run these code
monitorEvents($0, 'click')

// When click on that node
// click MouseEvent {isTrusted: true, screenX: 183, screenY: 180, clientX: 474, clientY: 34, …}
```