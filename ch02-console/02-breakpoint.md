# 02 Breakpoint

## 条件断点

### 1.Debugger中打条件断点

New Snippet

```javascript
for (var i = 0; i < 10; i++) {
    if (i === 6) {
        debugger;
    }
    "placeholder"; 
}

// Add Conditional Breakpoint i === 5
```

![breakpoint-condition](../.gitbook/assets/breakpoint-condition.webp)


### 2.忍者输出

因为console.log返回undefined即false，所以条件断点可以如下使用  
New Snippet

```javascript
var beg = "Console Time Here";  // Add Conditional Breakpoint console.time()
for (var i = 0; i < 10; i++) {
    ; 
}
var end = "Console TimeEnd Here"  // Add Conditional Breakpoint console.timeEnd()

// 拿到了程序执行时间 default: 0.14404296875ms
```


![breakpoint-ninja](../.gitbook/assets/breakpoint-ninja.webp)


PS:

* 断点详情右键可以disable或者remove所有断点
* log增加时间戳？Command+Shift+P =&gt; Show timestamps

