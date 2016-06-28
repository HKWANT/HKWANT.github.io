## css3选择器
### 子代选择器 vs 后代选择器
<pre>
- E>f VS E F
- 子元素选择器选中的是子元素F 子孙不会被选
- 后代选择器是选择所有的F 包括子子孙孙
</pre>
### 相邻兄弟选择器 VS 通用兄弟选择器
<pre>
- E+F VS E~F
- 都要同一父级
- 相邻兄弟选择器的重点是在相邻！通用兄弟选择区不需要！
- ex:div span+i
</pre>
### 属性选择器
<pre>
- E[attr]
- E[attr="value"]
- E[attr~="value"]表示几个以空格隔开idea属性值中包含了“value”
- E[attr^="value"]以value开头的值
- E[attr$="value"]以value结尾的值
- E[attr*="value"]包含了value得值
- E[attr|="value"]以value-开头
- E[attr="value"]和E[attr*="value"]是最实用的
</pre>
### 伪类选择器
<pre>
- 锚点伪类
- Ul元素伪类 表单元素
- :disabled :enabled :checked :focus(没有blur)
- ex:input[type="text"]:disabled{border:1px solid #999;background-color:#000}
</pre>
### nth选择器
<pre>
- :first-child选择某个元素的第一个子元素
- :last-child选择某个元素的最后一个子元素
- :nth-last-child()选择某个元素的一个或多个特定的子元素，从这个元素的最后一个子元素开始算
- :nth-of-type()选择指定的元素
- :nth-last-of-type()选择指定的元素，从元素的最后一个开始计算
- :first-of-type选择一个上级元素下得第一个同类子元素
- :last-of-type选择一个上级元素的最后一个同类子元素
- :only-child选择的元素它的父元素的唯一一个子元素
- :only-of-type选择一个元素是它的上级元素的唯一一个相同类型的子元素
- :empty选择的元素里面没有任何内容
</pre>
<pre>
- :nth-child()选择某个元素的一个或多个特定的子元素
- :nth-child(length)参数是具体数字
- :nth-child(n)参数是n，n从1开始计算
- :nth-child(2n)n的倍数选择，n从1开始算
- :nth-child(n+length)选择大于length后面的元素
- :nth-child(-n+length)选择小于length前面的元素
- :nth-child(2n+1)表示隔几选一（odd奇数  even偶数）
</pre>
### 否定选择器（:not）
- ex:input:not([type="submit"]){border:1px solid red;}
### 伪元素
<pre>
- ::first-letter选择文本块的第一个字母，除非在同一行里面包含一些其它元素，不过这个主要运用于段落排版上多
- ::first-line选择元素的第一行
- ::before,::after这两个主要用来给元素的前面或后面插入内容，这两个常用“content”配合使用，见过最多的就是清除浮动还有图片icon
- ::selection用来改变浏览网页选中文本的默认效果，“::selection”来改变在浏览器中选中文本后的背景色与前景色。 ::selection在IE家族中，只有IE9+版本支持，在Firefox中需要加上其前缀"-moz",:"::selection"只能设置两个属性，一个就是background,另一个就是color属性，设置其它属性是没有任何结果的
</pre>