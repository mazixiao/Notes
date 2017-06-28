### filter()用法 

```
filter()用法 ，函数返回true或false
它会跳过稀疏数组中缺少的元素，返回的数组总是稠密的，
	var a = [5, 4, 3, , , 2, 1];

	k = a.filter(function (x) {
		return x < 3;
	});
	console.log(k) //[2, 1]


	b = a.filter(function (x, i) {
		return i % 2 == 0;
	})
	console.log(b) //[5, 3, 1]
```



### every()和some()用法

```
every()和some()用法(注意:一旦every()和some()确定该返回什么值时就会停止遍历数组元素)
它们是数组的逻辑判定，返回true或false every()所有元素调用判定函数返回true，才返回true
	var a = [1, 2, 3];
	k = a.every(function (x) {
			return x < 4 //true
			//return x < 1 //false
		})
	console.log(k)

	//some()只要一个元素调用判定函数返回true，就返回true
	b = a.some(function (x) {
			return x < 4 //true
		})
	console.log(b)
```



### reduce()和reduceRight()用法

```
reduce()和reduceRight()可称为注入和折叠
	var a = [1, 2, 3, 4, 5];
	var sum = a.reduce(function (x, y) {
		return x + y;
	}, 0);
	console.log(sum); //15 (为0 + 1 + 2 + 3 + 4 + 5 = 15)

	var product = a.reduce(function (x, y) {
		return x * y;
	}, 2) 
	console.log(product) //120 (为2 * 1 * 2 * 3 * 4 * 5 = 240)

	var max = a.reduce(function (x, y) {//求最大值
		return x > y ? x : y;
	})
	console.log(max) //5



	var a = [1, 2, 3, 4, 5];
	var b = a.reduceRight(function (d, f) { //优先顺序从右到左处理数组
		return d * f;
	}, 2)
	console.log(b) //240
```



### indexOf()和lastindexOf()用法

```
indexOf()和lastindexOf()用法（数组和字符串都有该方法）
indexOf()从头至尾搜索，lastIndexOf()反向搜索
没有找到元素返回-1
	var a = [1, 2, 3, 4, 5];
	console.log(a.indexOf(1)) //0(索引)
	console.log(a.lastIndexOf(3))//2(倒过来找)
	console.log(a.indexOf(6));//-1(没有元素为6的索引)
```













