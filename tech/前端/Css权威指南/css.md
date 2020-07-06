![image-20200612204731360](F:\Code\github\document\InHackerWay\个人文章\读书笔记\前端\Css权威指南\css.assets\image-20200612204731360.png)


```
搜索图标
<button><img></button>>
border-radius:50% 椭圆或者圆 （边界半径）
object-fit:cover （图片不要缩放）
object-positon:left 图片的左边部分
```

边框虚线半径5个像素

![image-20200612224832871](F:\Code\github\document\InHackerWay\个人文章\读书笔记\前端\Css权威指南\css.assets\image-20200612224832871.png)

0 25%  左上角右下角0  右上角左下角25%

0 10% 25%  左上角0 左下角右上角10% 右下角25%

10px/100px 第一个是水平半径，第二个是垂直半径

![image-20200612225644351](F:\Code\github\document\InHackerWay\个人文章\读书笔记\前端\Css权威指南\css.assets\image-20200612225644351.png)

![image-20200612225812926](F:\Code\github\document\InHackerWay\个人文章\读书笔记\前端\Css权威指南\css.assets\image-20200612225812926.png)

box-shadow:0px 3px 5px(blurradio);3个像素阴影 模糊了另外5个像素 总共8个

box-shadow:0px 3px 15px 25px  第四个 扩展半径（负数为缩小）

box-shadow:+-3px 3px 第一个正是右边阴影，负左边阴影 其他同理

box-shadow 里面逗号隔开可以设置多个shadow.

![image-20200614162025095](F:\Code\github\document\InHackerWay\个人文章\读书笔记\前端\Css权威指南\css.assets\image-20200614162025095.png)

![image-20200614162142714](F:\Code\github\document\InHackerWay\个人文章\读书笔记\前端\Css权威指南\css.assets\image-20200614162142714.png)

带有蓝色框的阴影和4个单独白色框阴影的白色div

![image-20200614162254399](F:\Code\github\document\InHackerWay\个人文章\读书笔记\前端\Css权威指南\css.assets\image-20200614162254399.png)

```
div.card-inner {
  width: 100%;
  height: 100%;
  text-align: center;
  transform-style: preserve-3d;//3d
  transition: transform 1s;
}
```

```
div.card-front,
div.card-back {
  position: absolute;//--正反两面都在彼此的顶点
  width: 100%;
  height: 100%;
  backface-visibility: hidden;
  -webkit-backface-visibility: hidden;
}
```

```
div.card-back {
  background-color: #24cfa6;
  color: white;
  transform: rotateY(180deg);
}

```

卡片背面沿Y旋转180度，带颜色的绿色面孔背对着我们

 **`backface-visibility`** 指定当元素背面朝向观察者时是否可见。 

```
div.card-front,
div.card-back {
  position: absolute;
  width: 100%;
  height: 100%;
  backface-visibility: hidden;
  -webkit-backface-visibility: hidden;
}

```

 perspective: 1000px;  用这个才有翻转的效果



slow

![image-20200614154016432](F:\Code\github\document\InHackerWay\个人文章\读书笔记\前端\Css权威指南\css.assets\image-20200614154016432.png)



animation:6s infinit move alternate(反弹效果)

  linear  匀速

![image-20200614161305456](F:\Code\github\document\InHackerWay\个人文章\读书笔记\前端\Css权威指南\css.assets\image-20200614161305456.png)