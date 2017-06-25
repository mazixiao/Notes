## push()和pop()用法

```
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>数组方法push()和pop()用法</title>
</head>
<body>
<script>

	//push()在数组后面添加一个或多个元素，返回新数组的长度(切记是长度)
	//pop()删除数组最后一个元素，返回删除的值
	
	var a = [1, 2, 3, 4, 5];
	console.log(a.push(6, 7, 8)) //8， 新的数组长度为8
	console.log(a) //[1, 2, 3, 4, 5, 6, 7, 8]


	var b = [1, 2, 3, 4, 5];
	console.log(b.pop());  //5， 返回删除后的元素
	console.log(b); // [1, 2, 3, 4]

</script>	
</body>
</html>
```



