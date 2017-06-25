## unshift()和shift()用法

```
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>数组方法unshift()和shift()用法</title>
</head>
<body>
<script>

	// unshift()在数组最前面添加一个或多个元素，返回新数组的长度(切记是长度)
	// shift()删除数组第一个元素，返回删除的值
	
	var a = [1, 2, 3, 4, 5];
	console.log(a.unshift(7, 0)); // 7, 新的数组长度为7
	console.log(a); // [7, 0, 1, 2, 3, 4, 5]


	var b = [1, 2, 3, 4, 5];
	console.log(b.shift()); // 1, 返回删除后的元素
	console.log(b); //[2, 3, 4, 5]

	//补番
	console.log(new Date().toLocaleString()) //对数字、日期和时间做本地化的转换 //2017-6-25 13:51:15

</script>	 
</body>
</html>
```

