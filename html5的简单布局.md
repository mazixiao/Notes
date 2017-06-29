## html5的简单布局

```
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>html5代码实现</title>
</head>
<style>
	* {
		margin: 0;
		padding: 0;
		list-style: none;
	}
	nav {
		width: 100%;
		height: 100px;
		line-height: 100px;
		background: red;
		overflow: hidden;
	}
	li {
		text-align: center;
		float: left;
		background: cyan;
		width: 100px;
	}
	section {
		width: 100%;
		height: 200px;
		background: green;
		overflow: hidden;
	}
	aside {
		width: 200px;
		height: 100%;
		background: yellow;
		float: left;
	}
	article {
		width: 100%;
		height: 100%;
		background: pink;
	}
	/* 空的注释 */
	footer {
		width: 100%;
		height: 50px;
		background: blue;
	}
</style>

<body>
<header>
	<nav>
		<ul>
			<li>导航一</li>
			<li>导航二</li>
			<li>导航三</li>
		</ul>
	</nav>	
</header>
<!-- 章节	 -->
<section>
<!-- <aside> 标签定义 article 以外的内容。aside 的内容应该与 article 的内容相关。 -->
	<aside>侧边</aside>
	<article>文章</article>
</section>
<footer>
	脚
</footer>
</body>
</html>
```

## html    css   js的注释

```
<!-- html的注释	 -->



/* css的注释 */


// js的注释(单行)      /* */(多行)
```



```
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>h5代码实现布局</title>
	<style>
		header {
			height: 100px;
			background: red
		}
		section {
			height: 200px;
			overflow: hidden;
		}
		section nav {
			float: left;
			height: 200px;
			width: 200px;
			background: green;
		}
		section article {
			/* float: right; */
			height: 100px;
			background: yellow;
		}
		section footer {
			/* float: right; */
			height: 100px;
			background: blue;
		}
	</style>
</head>
<body>
<header>头</header>	
<section>
	<nav>导航</nav>
	<article>内容</article>
	<footer>脚</footer>
</section>
</body>
</html>
```



