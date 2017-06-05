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



