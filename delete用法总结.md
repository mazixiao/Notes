## delete用法

```
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>delete用法</title>
</head>
<body>

<script>

	//delete希望操作数是左值，(x = 1),如果不是左值，delete不进行任何操作并返回true，
	
	//内置核心和客户端属性不能删除
	//通过var定义的变量也不能删除
	//通过function定义的函数和函数参数也不能删除
	var a = {
		x: 1,
		y: 2,
	} 
	console.log(delete a.x) //true
	console.log(typeof a.x); //属性不存在,返回undefined
	console.log(typeof a.y); //number;
	console.log(delete a.x); //删除一个不存在的属性， true
	console.log(delete k); //删除一个不存在的变量，true
	console.log(delete a); //不能删除通过var定义的变量，false
	console.log(delete 1); //参数不是一个左值，返回true
	console.log(this); //window对象

	this.x = 1; //给全局变量定义一个属性，这里没有使用var
	console.log(delete x) //非严格模式下为true，严格模式下回报错，可以使用delete this.x

	function f() {

	}
	console.log(delete f);//false


</script>	
</body>
</html>
```

