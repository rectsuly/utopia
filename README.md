## 1 新建项目

最开始只保留了pages文件夹和project.config.json文件。

新建app.js和app.json文件。

在小程序开发工具里新建页面，提示新建页面失败，原因是app.js和app.json文件初始化不能为空，需要在app.js里加上App()，在app.json加上{}。修改好之后新建一个classic页面，app.json会自动把classic页面的路径添加到pages属性。小程序所有页面都必须在app.json里面注册。

重新在pages下面新建一个classic文件夹，把之前的页面删除了在文件夹里创建页面。

小程序没有onLaunch函数会报错。在app.js文件的App()里新建一个对象{}，里面的内容是onLaunch:function(){}。

app.json配置项，配置window大项和子项。

在根目录下新建一个components文件夹，新建like文件夹，新建index页面。

在classic文件夹下的classic.json添加usingComponents属性值:"components/like/index"。

## 2 编写like组件

在components/like目录下新建images目录并导入素材图片。

在index.wxml和index.wxss中编写点赞心形组件代码。

在根目录下创建app.wxss文件，添加page{}里的font-family为"PingFangSC-Thin"。

```css
.container {
  display: inline-flex;
  flex-direction: row;
}

.container image{
  width: 32rpx;
  height: 28rpx;
}

.container text {
  font-size: 24rpx;
  line-height: 24rpx;
  color:#bbbbbb;
  position: relative;
  bottom: 10rpx;
  left: 6rpx;
}
```
设置字体行高来消除字体的间距：line-height:24rpx;
设置display为inline-flex来使container的宽度自适应。






