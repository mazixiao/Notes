## concat() 方法用于连接两个或多个数组。

```

	<!DOCTYPE html>
	<html lang="en">
	<head>
		<meta charset="UTF-8">
		<title>concat() 方法用于连接两个或多个数组。</title>
	</head>
	<body>
		<script>
		//concat() 方法用于连接两个或多个数组。
		var a = ["1", "2", "3"];

		var b = ["aa", "bb", "cc"];
		console.log(a.concat(b)) //创建一个新的数组 ["1", "2", "3", "aa", "bb", "cc"]]

		console.log(b.concat(a)) //创建一个新的数组 ["aa", "bb", "cc", "1", "2", "3",]]
        console.log(a) //原数组不变
        console.log(b) //原数组不变

		</script>
	</body>
	</html>
```

