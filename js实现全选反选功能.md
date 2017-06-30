## 用js实现全选和取消全选功能

```
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>用js实现全选和取消全选功能</title>
</head>
<body>
	<input type="checkbox" id="checkall">全选
	<div>
		<input type="checkbox" name="type" value="1">这是1
		<input type="checkbox" name="type" value="2">这是2
	</div>	
<script>
	var checkall = document.getElementById("checkall");
	var div = document.querySelector("div");
	var one = div.children[0];
	var two = div.children[1];
	checkall.onclick = function () {
	for (var i = 0; i < div.children.length;i++) {
		div.children[i].checked = this.checked;	
	}	
	}
</script>
</body>
</html>
```

