### 看板娘

[http://demo.frontendx.cn/live2d-example/index.html](http://demo.frontendx.cn/live2d-example/index.html)

### 前言

下面我将简单粗暴滴给小伙伴们介绍下怎么配置`二次元`看板娘。

本妹子的看板娘先给各位主人来露个脸吧！请多多关照^ ^
[http://demo.frontendx.cn/live2d-example/index.html](http://demo.frontendx.cn/live2d-example/index.html)

![image.png](https://upload-images.jianshu.io/upload_images/9902136-da6e3dbb39e05416.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

### 用法

Talk is cheap. Show me the code.

第一步：引用文件`L2Dwidget.min.js`,地址为[https://l2dwidget.js.org/lib/L2Dwidget.min.js](https://l2dwidget.js.org/lib/L2Dwidget.min.js)

第二步：引用对应动画精灵的`json`文件，引用动画精灵地址为：[https://github.com/xiazeyu/live2d-widget-models](https://github.com/xiazeyu/live2d-widget-models)

第三步：初始化看板娘
```javascript
L2Dwidget.init({
    "model": { "jsonPath": "packages/live2d-widget-model-shizuku/assets/shizuku.model.json" }
});
```
三步搞定是不是很简单。它会自动在页面中生成`id`为`live2d-widget`的`dom`元素，这就是你的看板娘。还想多DIY下的小伙伴们可以接着往下看～

### 进阶用法

> 只有部分看板娘才有进阶用法

#### 事件监听

可以添加事件监听，比如触摸她的时候会弹出点提示
```javascript
L2Dwidget.on('*', (name) => {
    console.log('事件为： ' + name)
})
```
#### 显示对话框

当触摸到角色身体或脸时，弹出对话框。
```javascript
L2Dwidget.init({
    dialog: {
        enable: true,
        script: {
            'tap body': '哎呀！别碰我！',
            'tap face': '人家是在认真写博客哦--前端妹子',
        }
    }
});
```
#### 看板娘位置

位置默认在左下角，还可以设置`right` `top`
```javascript
L2Dwidget.init({
    display: {
        position: 'right'
    }
});
```
#### 移动端兼容配置

可以设置在移动端是否显示，或者缩小显示
```javascript
L2Dwidget.init({
    "mobile": { "show": true, scale: 0.5 },
});
```
### 案例

还迷茫的小伙伴看直接看我写的`demo`：
[http://raoenhui.github.io/domes/live2d-example/index.html](http://raoenhui.github.io/domes/live2d-example/index.html)

通过`demo`，看板娘有以下可选择：
  - `chitose`
  - `Epsilon2.1`
  - `Gantzert_Felixander`
  - `haru01`
  - `haru02`
  - `haruto`
  - `hibiki`
  - `hijiki`
  - `izumi`
  - `koharu`
  - `miku`
  - `nico`
  - `ni-j`
  - `nipsilon`
  - `nito`
  - `shizuku`
  - `tororo`
  - `tsumiki`
  - `Unitychan`
  - `wanko`
  - `z16`

### 插件

很多有hexo搭博客的小伙伴们可以直接安装[hexo-helper-live2d](https://github.com/EYHN/hexo-helper-live2d)插件

用了`pixijs`动画引擎的，也可以用[pixi-live2d](https://github.com/avgjs/pixi-live2d)插件

### 其他YY

看板娘主要以`Live2D`为核心引擎，[Live2D](https://live2d.github.io/)主要是有日本Guyzware公司开发的，支持native和web端，如果想自定义些功能的小伙伴们，可以研究下案例[https://live2d.github.io/CubismJsComponents/](https://live2d.github.io/CubismJsComponents/)。

虽然本妹子很想进入游戏开发，但是技术有限，至今仍在零基础徘徊，略显尴尬 .但是有绘画基础的小伙伴们可以给自己的`blog`请了一位喜欢唱，跳，rap和篮球的看板娘哦。


Happy coding .. :)

### 相关链接

[http://demo.frontendx.cn/live2d-example/index.html](http://demo.frontendx.cn/live2d-example/index.html)

[http://raoenhui.github.io/domes/live2d-example/index.html](http://raoenhui.github.io/domes/live2d-example/index.html)

[https://l2dwidget.js.org/docs/index.html](https://l2dwidget.js.org/docs/index.html)

[https://github.com/xiazeyu/live2d-widget.js](https://github.com/xiazeyu/live2d-widget.js)

[https://www.live2d.com/](https://www.live2d.com/)

[https://live2d.github.io/CubismJsComponents/](https://live2d.github.io/CubismJsComponents/)
