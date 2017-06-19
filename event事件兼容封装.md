## event事件兼容封装

```
//添加事件
function addEvent(element, type, fn){
    //能力检测
    if(element.addEventListener){
        element.addEventListener(type, fn, false);
    }else if(element.attachEvent){
        element.attachEvent("on"+type, fn);
    }else {
        //如果都不行，那就用on方式
        element["on"+type] = fn;
    }
}


//移除事件
function removeEvent(element, type, fn) {
    if(element.removeEventListener){
        element.removeEventListener(type, fn, false);
    }else if(element.detachEvent){
        element.detachEvent("on"+type, fn);
    }else {
        element["on"+type] = null;
    }

```

## 事件对象

```
事件对象，只要触发某个元素的绑定的事件，就会产生事件对象event，包含了触发事件的元素，事件的类型，和事件其他的一些相关信息。
```





## 给多个input框注册委托事件

```
<!doctype html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>
<body>
    <div>
        <input type="text">
        <input type="text">
        <input type="text">
        <input type="text">
    </div>
<script>
    //事件对象，只要触发某个元素的绑定的事件，就会产生事件对象event，
    // 包含了触发事件的元素，事件的类型，和事件其他的一些相关信息
    var body = document.getElementsByTagName("div")[0];
    if (body.addEventListener) {//判断谷歌的兼容，如果浏览器支持addEventListener，执行下面的代码
        body.addEventListener("focus", function (e) { //focus获得焦点 blur失去焦点
            e = window.event || e;
            var target = e.srcElement || e.target;
            console.log(new Date());
        }, true) //在捕获阶段，才可以给input注册事件代理 ，为false 冒泡阶段
    } else if (body.attachEvent) {//判断ie的兼容，如果浏览器支持attachEvent，执行下面的代码
        body.attachEvent("onfocusin", function (e) { //在ie下给input注册事件委托时候，onfocusin获得焦点 onfocusout失去焦点
            e = window.event || e;
            var target = e.srcElement || e.target;
            //debugger;
                console.log("attachEvent" + new Date());

        })
    }
</script>

</body>
</html>
```

