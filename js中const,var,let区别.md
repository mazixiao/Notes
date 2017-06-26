## var、 let 、const定义变量的区别之处

```
//1.const定义的变量不可以修改，而且必须初始化。
	//
	// const a = 1;
	// a = 2;
	// console.log(a) //报错
	
//2.var定义的变量可以修改，如果不初始化会输出undefined，不会报错。

//3.let是块级作用域，函数内部使用let定义后，对函数外部无影响，如果不初始化会输出undefined，不会报错。

	function a() {
		let c = 6;
		console.log(c) //6
	}
	a()

	let c = 3;
	console.log(c) //3
```

