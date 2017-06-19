## （条件判断语句: if、else if、switch）switch语句

```
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>test</title>
</head>
<body>

	<script>
	var day=new Date().getDay();//getDay() 方法可返回表示星期的某一天的数字。
	console.log(day); //5，今天星期五
	switch (day)
	{
	case 0:
	  console.log("星期日");
	  break;  //break是跳出整个循环体，continue是结束单次循环 //如果在函数中使用break，也可以用return来代替。
	case 1:
	  console.log("星期一")
	  break;
	case 2:
	  console.log("星期二")
	  break;
	case 3:
	 console.log("星期三")
	  break;
	case 4:
	  console.log("星期四")
	  break;
	case 5:
	 console.log("星期五")
	  break;
	case 6:
	  console.log("星期六")
	  break;
	default: //所有条件都不匹配 ，如果没有default标签，则整个语句都将跳过，可以放在switch语句的任何地方
		console.log("出错");
		break;
	}
	
	
	//更贴近实战
    	function didi(x) {	
			switch(typeof x) { //判断传入数据的类型
				case "number": 
				return x; //122
				case 'string':
				return '"'+ x +'"';  //"122"
				default:
				return String(x); //使用普通方法转换其他类型
			}
		}
		
		console.log(didi(122))
		console.log(didi("122"))
	
	</script>	
</body> 
</html>
```

