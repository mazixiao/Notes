## 将for循环里的i赋给一个全局变量

```
window.onload = function () {
	var body = document.getElementsByTagName("body")[0];
	var q = location.search; //获取上一个页面传入的id值 
	//console.log(q); //"?id=2"
	//console.log(location.search.length);
	var k = q.slice(4, q.length);
	console.log("跳转的id值--->"+k)//获取id值  
	//console.log(k)//获取id值  

	
	//创建对象
	var xhr = new XMLHttpRequest();
	//建立连接
	xhr.open("get", "data.json");
	//发送数据
	xhr.send(null);
	//接收数据
	xhr.onreadystatechange = function () {
		if (xhr.readyState == 4 && xhr.status == 200) {
			var data = xhr.responseText;
			var obj = JSON.parse(data);
			 
			 var a; //创建一个全局变量a
			
			for ( var i = 0; i < obj.length; i++) {
				//console.log(obj[i].id)
                if (k == obj[i].id) { 判断，如果从上个页面传入的值和遍历的值一样，就执行下面的代码
                    a = i; //把确定的那个i赋给a，或者a = obj[i]; 则body.children[0].innerHTML = a.name;
				}				
			};
			console.log("a的值"+a);
			    body.children[0].innerHTML = obj[a].name;			
                body.children[1].innerHTML = obj[a].sex;			
                body.children[2].innerHTML = obj[a].age;
		};
	};	
	body.children[3].onclick = function () {
		history.go(-1);
		//input.onclick();
	}
	
}
```

## 或者这样做

```
for ( var i = 0; i < obj.length; i++) {
					if (k  == obj[i].id) { //如果k的值和遍历的id值相同，就跳出循环体
						console.log(obj[i].id);
						break;
						
					}
				};
				 body.children[0].innerHTML = obj[i].name;			
                 body.children[1].innerHTML = obj[i].sex;			
                 body.children[2].innerHTML = obj[i].age;
```

## 最简单

```
for ( var i = 0; i < obj.length; i++) {
					if (k  == obj[i].id) {
				 body.children[0].innerHTML = obj[i].name;			
                 body.children[1].innerHTML = obj[i].sex;			
                 body.children[2].innerHTML = obj[i].age;
					}
				};
```

