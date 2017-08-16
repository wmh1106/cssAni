# less变量的引用、拼接、字符串插值

# less 循环

```less
.loop-li(@n) when ( @n > 0 ) {
	
	@name:~"ani@{n}";
	.aniSign li:nth-of-type(@{n}){
		left:10% * @n;
		background-image: url('../img/p@{n}-2.png');
		animation-name:@name;
	}

	.loop-li(( @n - 1 ));
}

.loop-li(7) ;
```

# 监听Animation动画事件

1. 动画开始时：webkitAnimationStart
2. 动画结束时：webkitAnimationEnd
3. 动画再一次重复时：webkitAnimationIteration

使用：

`element.removeAttribute('webkitAnimationIteration',fnSign,false);`

`element.addEventListener('webkitAnimationIteration',fnSign,false);`