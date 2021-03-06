## loiter
一款基于原生js的组件，灵感来于知乎登陆页背景，比[particles.js](https://github.com/VincentGarreau/particles.js)更加轻量。  
[demo](http://www.chengfeilong.com/loiter.js)
## 使用方式
在html结构中写入id为loiter的canvas标签，引入loiter.js或者压缩版loiter.min.js，然后调用loiter.start();，选择是否配置默认项，具体配置例在最底部。  
html
```html
<canvas id="loiter"></canvas>
<script src="loiter.js"></script>
<script>
    loiter.start();
</script>
```
效果：  
![default](./images/default.gif)
## 配置对象

| 参数名         | 可选值         | 描述                          |
|:------------- |:-------------:|:-----------------------------|
| width         | /             |容器宽度，默认窗口宽度            |
| height        | /             |容器高度，默认窗口高度            |
| num           | /             |圆点个数，默认17个               |
| container     | /             |容器，默认id="loiter"的canvas标签|
| FPS           | /             |绘制刷新率，默认60               |
| mode          | impact/through |圆点到达边界后的效果，impact为到达后碰撞返回效果，through为到达后穿过效果，默认为impact|
| circleColor   | /             |圆点颜色，默认为灰色              |

考虑到线条的渐变效果，所以线条颜色和粗细不可设。  
调用方式：  
js

```js
<script>
    loiter.start({
        width:700,
        height:300,
        num:31,
        container:document.getElementsByTagName('canvas')[0],
        FPS:200,
        mode:'through',
        circleColor:'red'
    });
</script>
```
配置：  
![config](./images/config.png)  

效果：  
![skyblue](./images/skyblue.gif)
