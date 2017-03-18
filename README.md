# 妙味整站制作

整站CSS完成后:   
1,处理IE6下PNG文件不能识别的问题.  
可以用IETESTER测试一下,更好的要用原生的IE6来测试. 
引入一个JS文件
DD_belatedPNG_0.0.8a.js
再在body里面写入以下代码即可.
 
```
<!--[if IE 6]>
	<script src="js/DD_belatedPNG_0.0.8a.js" type="text/javascript"></script>
	<script type="text/javascript">DD_belatedPNG.fix('*');</script>
<![endif]-->
```
