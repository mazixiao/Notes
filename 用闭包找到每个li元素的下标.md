## 用闭包找到每个li元素的下标

```
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>用闭包找到每个li元素的下标</title>
</head>
<body>
	<ul id="list">
		<li>11</li>
		<li>22</li>
		<li>33</li>
		<li>44</li>
		<li>55</li>
	</ul>
<script>
	var ul = document.getElementById("list");
	var lis = ul.children;

	for (var i = 0; i < lis.length; i++) {

		(function(i) {
			lis[i].onclick = function() {
				console.log(i);
			}
		})(i);


		// function outer () {
		// 	var j = i;
		// 	function inner() {
		// 		console.log(j);
		// 	}
		// 	return inner;
		// }
		//  lis[i].onclick = outer();
	}
</script>
</body>
</html>
```

