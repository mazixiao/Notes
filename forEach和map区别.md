## forEach和map区别

```
	var ary = [12, 23, 24, 42, 1];

	var res = ary.forEach(function (item,index,input) {
	    input[index] = item * 10;
	})
	console.log(res);//-->undefined;
	console.log(ary);//-->forEach会对原来的数组产生改变, [120,230,240,420,10];




	var ary = [12, 23, 24, 42, 1];
	
	var res = ary.map(function (item,index,input) { //传递给map()的函数应该有返回值
	    return item * 10;
	})
	console.log(res);//-->[120,230,240,420,10];//返回一个新的数组
	console.log(ary);//-->map不会修改原来的数组，[12,23,24,42,1];
```

