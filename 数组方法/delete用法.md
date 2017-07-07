### 数组的delete用法

```
<script>
	
	var a = [1, 2, 3]; 
	
	delete(a[0])
//detele只能删除数组元素的值，所占空间还在，总长度没变
	console.log(a) //[undefined × 1, 2, 3]
	
	
</script>
```

