---
title: markdown 语法
date: 2019-02-12 10:59:33
tags:
---

### 这是h2标题
**这是加粗的字体**
*这是斜体*
***斜体加粗***
~~删除线文字~~

>这是引用
>>二级引用
>>>三级了
>>二级

****
上面分割线不成功？
![这是图片](https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1529733303471&di=451ddd05dd47323e509db124d5611b17&imgtype=0&src=http%3A%2F%2Fimg.25pp.com%2Fuploadfile%2Fsoft%2Fimages%2F2013%2F0103%2F20130103033541695.jpg "这是title")
![这是本地图片](timg.jpg)
{% asset_img timg.jpg This is an example image %}


[超链接百度](http://www.baidu.com "这是超链接title")
[超链接本地](/about)

- 无序列表
* 无序列表
+ 无序列表

1.有序列表
2.有序列表

* 列表嵌套
   * 列表嵌套
      * 又一级
         1. 啊啊啊
         2. 不不不

`console.log('aa')`

```php
function(){
    echo '这是一段牛逼的代码';
}
```


表格 | Academy | score
- | :-: | -:
Harry Potter | Gryffindor| 90
Harry Potter | Gryffindor啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊| 90

<div class="tip">
    预处理器很强大，但它只是编写 CSS 的辅助工具。出于对扩展和维护等方面的考虑，在大型项目中有必要使用预处理器构建 CSS；但是对于小型项目，原生的 CSS 可能是一种更好的选择。不要肆意使用预处理器！
</div>