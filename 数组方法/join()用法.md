## join()用法

```
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>数组的join()用法</title>
</head>
<body>
<script>
	//join()把数组里所有元素转化为字符串并连接在一起，返回最后生成的字符串，元素是通过指定的分隔符进行分隔的。
	
	var a = [1, 2, 3, 4];

	console.log(a.join()) //1,2,3,4

	console.log(a.join(" ")) //1 2 3 4
	
</script>	
</body>
</html>
```

