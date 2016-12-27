[代码演示地址](http://6.lcdmx.applinzi.com/)

输入字母实现自动模糊查询

PS：
1.当把搜索框清空时，搜索结果也会清空
2.双击查询到的单词会返回顶部


使用autocomplete插件
```
$("#condition").keyup(function(){
			oWord = $("#condition").val();
			if (oWord=="") {
				$(".result").html("");
			}
});

$('#condition').autocomplete(allOptions,{max:6,}).result(function(event, data, formatted) {
	     $(".result").append("<a href='#" + data +"'>" + data + "</a><br />");
});
```
