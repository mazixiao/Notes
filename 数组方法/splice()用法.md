## splice()用法

```
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>数组方法的splice()用法</title>
</head>
<body>
<script>

	//splice(start, end)会修改原来的数组
	//返回的新数组从start开始，朝后数end个元素
	//如果只有start，则返回的元素从start到最后一个元素
	
	var a = [1, 2, 3, 4, 5];

	
	console.log(a.splice(1, 2)) //下标1开始，朝后数2个数 [2, 3] 

	console.log(a)  //返回删除后的元素 [1, 4, 5]


	var b = [1, 2, 3, 4, 5, 6, 7, 8];
	console.log(b.splice(3, 3)); //[4, 5, 6]
	console.log(b); //[1, 2, 3, 7, 8]

</script>	
</body>
</html>
```

