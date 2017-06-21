## 打印event.keyCode

```
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>event.keyCode</title>
</head>
<body>

请输入号码<input type="text">

<script>
//keyCode 属性返回onkeypress事件触发的键的值的字符代码，或者 onkeydown 或 onkeyup 事件的键的代码。

	var input = document.getElementsByTagName("input")[0];

    // input.onkeyup = function (event) {

    // 	console.log(event.keyCode);	//打印键盘上键盘码
    // 	console.log(event.key);	//打印键盘上真实的键值

    // }


    input.onkeydown = function(e){ 

		// e = e ? e : window.event;
		e  = e || window.event; //兼容ie

		//var keyCode = e.which ? e.which : e.keyCode;    
		var keyCode = e.keyCode; //获取键盘码
		console.log(e.keyCode);
	}
</script>
	
</body>
</html>
```

