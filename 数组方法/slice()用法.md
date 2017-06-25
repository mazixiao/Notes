## slice()用法

```
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>数组方法的slice()用法</title>
</head>
<body>
<script>

	//slice(start, end)不会修改原来的数组或字符串,返回的数组或者字符串包含start但不包含end.
	//当只有一个参数，返回的是该参数到结尾的所有元素.
	//-1 指最后一个元素，-2 指倒数第二个元素

	var a = "12345";
	console.log(a.slice(1, 3)); //23



	var b = [1, 2, 3, 4, 5];

	console.log(b.slice(0, 3)); //[1, 2, 3]

	console.log(b.slice(2)); //[3, 4, 5];

	console.log(b.slice(1, -1)); //[2, 3, 4]

	console.log(b.slice(-3, -2)); //[3]

</script>	
</body>
</html>
```

