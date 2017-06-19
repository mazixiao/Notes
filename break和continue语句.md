## break和continue语句

```
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>test</title>
	<script type="text/javascript">
		//将1-10之间的第一个是2的倍数的数字输出
		for (var i = 1; i <= 10; i++) {
			if (i%2 == 0) {
				console.log(i); //2
				break; //跳出循环体
			}
		}


		//将1-10除6以外的数字输出到控制台
		  for (var i = 1; i <= 10; i++) {
		  		if (i == 6) {
		  			continue;     //跳过本次循环
		  		}
		  		console.log(i); //1 2 3 4 5 7 8 9 10
		  }

	</script>
</head>
<body>
	
</body>
</html>
```

