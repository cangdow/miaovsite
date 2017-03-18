# 妙味整站制作

整站CSS完成后:
#### 政府,电商之类网站才要支持IE6,本质也是因为XP占有率高.   
1,处理IE6下PNG文件不能识别的问题.  
可以用IETESTER测试一下,更好的要用原生的IE6来测试. 
引入一个JS文件
DD_belatedPNG_0.0.8a.js
再在body里面写入以下代码即可.
 
```
<!--[if IE 6]>
	<script src="js/DD_belatedPNG_0.0.8a.js" type="text/javascript">
	</script>
	<script type="text/javascript">DD_belatedPNG.fix('*');</script>
<![endif]-->
```
2,IE6下行高无法针对图片来应用.

```
/* 解决IE6下图片不兼容问题, 尽量不要用CSS hack方法.*/
.sbie6_img img{float: left;position: relative;top: 10px;}
```
3,IE6下input框内文字不会居中问题.

```
.search .text{width: 230px;height: 31px;position: absolute;top: 0;
left: 20px;background: none;border:none;
	font-size: 13px;color:#666;}
/* IE6下input内容不居中问题 */
.search .text{line-height: 30px;}
```
4,IE6下a标签光标不会出现手的问题

```
/* IE6下a标签光标不会出现手的问题 */
#nav a{cursor:pointer;}
```
5,IE6下PNG改成GIF就能适应了.不然会有0.5px偏差.
也就是说如果不需要透明,又要兼容的时候,存成GIF就好了.

6,IE6下a链接鼠标原标签和hover都要设置text-decoration:none;才不会有.