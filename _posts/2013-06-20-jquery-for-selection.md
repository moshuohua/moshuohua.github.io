---
layout: post
title: 使用JQuery实现选择文本弹出Popover 
category: code
---

#{{ page.title }}

<p class="meta">20 六月 2013</p>

这两天看了 [Medium](http://medium.com) 的Note功能，感觉非常棒，不是单纯的针对整篇文章进行评论，从而更加具有针对性，虽然有一定的缺点，但是也不失为一种解决方案，日后有机会可以在此基础上微创新一下，或综合一下。

但这不是这篇文章的重点，从技术角度来讲，我不熟悉JS，只会简单用用Jquery，所以就用它做了一个那个效果的模仿，虽然解决方案很简陋，但是有点效果，过几天用Rails写个站试试，用作comment的前端方案。

除了Jquery，还使用了以下东西：

Popover的选择：[Todc-Bootstrap](http://todc.github.io/todc-bootstrap) 这是仿照Google风格的bootstrap版本，非常好用，界面也不错，这里使用popover

Selection的库：[JQuery++](http://jquerypp.com/#range) 是对jquery的补充的一个插件集，可以针对自己的需要下载相应功能的插件，我这里使用的是range插件

高亮的插件：[Highlight](http://johannburkard.de/blog/programming/javascript/highlight-javascript-text-higlighting-jquery-plugin.html) 很简单的需求，直接用插件解决得了

![效果图](/assets/img/4.png)

代码中有详细注释：

```javascript
$('#text').mouseup(function(){
	var range = $.Range.current();  //获取selection对象
	var start = range.start().offset,  //文本起始位置
		end = range.end().offset,  //结束位置
		ranger = range.toString();   //selection字符串
			
		if(end - start != 0){	//排除光标点击一下的情况
		
			//替换文本为加入tag的样式，从而使用popover
			$("div:contains('" + ranger + "')").each(function() {
                var newText = $(this).html().replace(ranger, 
					"<span class='item' rel='popover' data-placement='top'>" 
						+ ranger + "</span>");
                    $(this).html(newText);
                });
				

                $("#status").html("起始位置 = " + start
                        + "<br />结束位置 = " + end
                        + "<br />已选择文本 = " + ranger
                );
				
				//Bootstrap的popover的content做自定义返回内容
				$('.item').popover({ 
					html : true,
					content: function() {
						return $('#popover_content_wrapper').html();
					}
				});
				$('.item').popover('show');
                $('.item').highlight(ranger);  //高亮添加了tag的文本，即选中文本
            };
        });

        $('html').mousedown(function(){
            $('.item').popover('hide');  //鼠标落下事件隐藏popover
            $('span').contents().unwrap();	//去除选择文本的tag
        });
```





