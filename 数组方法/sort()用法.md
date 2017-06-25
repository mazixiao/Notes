## 数组方法的sort()用法

```
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>数组方法的sort()用法</title>
</head>
<body>
<script>
	//sort()方法将数组中的元素排序并返回排序后的数组，当不带参数调用sort()方法时，数组元素以 字母表顺序 排序(如有必要将临时转换成字符串进行比较)
	var a = ["b", "a", "c"];
	console.log(a.sort()); //["a", "b", "c"] //字母表顺序排序


	//如果包含undefined元素，将会排到数组的尾部
	var b = ["1", "a", null, undefined, 1, "b", null];
	console.log(b.sort()) //["1", 1, "a", "b", null, null, undefined]



	var c = [33, 4, 1111, 222];


	console.log(c.sort())  //[1111, 222, 33, 4]  //字母表顺序排序


	c.sort(function (a, b) {
		return a - b;
	});
	console.log(c); //[4, 33, 222, 1111] //数值排序


	c.sort(function (a, b) {
		return b - a;
	});
	console.log(c) // [1111, 222, 33, 4] //数值大小相反排序


	var d = ["ant", "cat", "Dog", "Bug"];
	console.log(d.sort()); // ["Bug", "Dog", "ant", "cat"]
	//不区分大小写
	d.sort(function (s, t) {
		var a = s.toLowerCase(); //转成小写
		var b = t.toLowerCase()
		if (a < b) {
			return -1;
		}
		if (a > b) {
			return 1;
		}
		return 0;
	})
	console.log(d) //["ant", "Bug", "cat", "Dog"]

</script>
</body>
</html>
```

