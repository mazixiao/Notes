## eee

```
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>slice,substr和substring的区别</title>
</head>
<body>

<script>

	//slice,substr和substring的区别
	//首先，他们都接收两个参数，slice和substring接收的是起始位置和结束位置(不包括结束位置)，
	//而substr接收的则是起始位置和所要返回的字符串长度。
	
	var test = 'hello world';

	console.log(test.slice(4, 7));             //o w
	console.log(test.substring(4, 7));         //o w
	console.log(test.substr(4, 7));            //o world

	console.log(test.slice(4));            	//o world
	console.log(test.substring(4));        	//o world
	console.log(test.substr(4));            //o world

	//这里有个需要注意的地方就是：substring是以两个参数中较小一个作为起始位置，较大的参数作为结束位置。
	console.log(test.substring(7, 4))   //o w

	//当接收的参数是负数时，
	//slice会从最后一个字符串计算
	//substring则返回整个字符串（一个参数）
	//substring则仅仅是将第一个参数的大小作为截取的长度（两个参数）
	//substr则干脆将负参数都直接转换为空字符串（两个参数）

	console.log(test.slice(-3));         //rld
    console.log(test.substring(-3));     //hello world
    console.log(test.substr(-3));        //rld

    console.log(test.slice(3, -4));       //lo w
    console.log(test.substring(3, -4));   //hel
    console.log(test.substr(3, -4));      //空字符串

</script>

</body>
</html>
```



