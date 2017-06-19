## cookies,sessionStorage和localStorage的区别

Web Storage有两种形式(h5中)：

LocalStorage（本地存储）和sessionStorage（会话存储）。

Web Storage数据完全存储在客户端，能够存储更多的数据，大概5M左右。

localStorage：浏览器关闭了数据仍然可以保存下来，并可用于所有同源（相同的域名、协议和端口）窗口（或标签页）永久存储，永不失效，除非手动删除

sessionStorage：数据存储在窗口对象中，窗口关闭后对应的窗口对象消失，存储的数据也会丢失。就是浏览器窗口关闭就失效了。



Storage类的相关成员如下：

| 成员名                | 方法参数            | 描述                         |
| ------------------ | --------------- | -------------------------- |
| length             | 属性              | 获取存储数据的条数                  |
| key(n)             | n:索引值           | 根据索引值，返回键名                 |
| getItem(key)       | key:键名          | 根据键名，获取数据值                 |
| setItem(key,value) | key:键名 value:键值 | 根据键名和键值设置数据项，如果键名已经存在，则覆盖值 |
| removeItem(key)    | key:键名          | 根据键名删除一个数据项                |
| clear()            | 无               | 清空当前的Storage对象             |







# cookie

单个cookie在客户端的存储量大概4k

Cookie的作用是与服务器进行交互，作为HTTP规范的一部分而存在，数据保存在浏览器端

cookie的有效期通过max-age设置，单位是秒。

path是相同协议 域名 端口 下的cookie值可以共享.

domain是允许二级域名不同的cookie值共享.



