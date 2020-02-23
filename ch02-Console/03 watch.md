
# 03 Watch  

## 变量监控

1. ### 监控变量

``` javascript
var objA = {a: "a", b: "b"};

// 点击控制台上小眼睛 Create Live Expression 输入ObjA
// 1 监测到c添加
objA.c = 10;
// 2 查看c的变化
for (var i = 0; i < 10; i++) {
    setTimeout(() => objA.c++, i * 1000);
}
```

2. ### Watch
debugger面板的watch具有类似功能

