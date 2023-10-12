<link rel="stylesheet" href="/ErhailakeUI/ErhaiLakeUI/css/ErhaiLakeUI.css">
<link rel="stylesheet" href="/ErhailakeUI/css/demo.css">
<style>
@font-face {
    font-family: "ErhaiLakeUI-icon";
    src: url('/ErhailakeUI/ErhaiLakeUI/fonts/iconfont.woff2') format('woff2'),
        url('/ErhailakeUI/ErhaiLakeUI/fonts/iconfont.woff') format('woff'),
        url('/ErhailakeUI/ErhaiLakeUI/fonts/ErhaiLakeUI-icon.ttf') format('truetype');
}
.icon_lists{
    display: flex;
    flex-wrap: wrap;
}
</style>
<script src="/ErhailakeUI/ErhaiLakeUI/js/ErhaiLakeUI.js"></script>

# icon

> [!NOTE]
> ErhaiLakeUI-icon采用字体形式,取材于 [阿里巴巴矢量图标库iconfont](https://www.iconfont.cn) ,因此可以把每一个 `icon` 看作是一个个普通的文字,直接通过 css 即可设定其样式.
> 支持 `Unicode Font-class Symbol` 三种格式.

## 示例

<!-- tabs:start -->

<!-- tab:预览 -->

<!-- tabs:start -->

<!-- tab:Unicode -->

<span class="ErhaiLakeUI-icon">&#xe613;</span>

<!-- tab:Font class -->

<span class="ErhaiLakeUI-icon ErhaiLakeLogo"></span>

<!-- tab:Symbol -->

<svg class="svg-icon" aria-hidden="true">
    <use xlink:href="#ErhaiLakeLogo"></use>
</svg>

<!-- tabs:end -->

<!-- tab:</> -->

<!-- tabs:start -->

<!-- tab:Unicode -->

```html
<span class="ErhaiLakeUI-icon">&#xe613;</span>
```

<!-- tab:Font class -->

```html
<span class="ErhaiLakeUI-icon ErhaiLakeLogo"></span>
```

<!-- tab:Symbol -->

```html
<svg class="svg-icon" aria-hidden="true">
    <use xlink:href="#ErhaiLakeLogo"></use>
</svg>
```

<!-- tabs:end -->

<!-- tabs:end -->

你可以很方便的去定义它的颜色或者大小:

<!-- tabs:start -->

<!-- tab:预览 -->

<!-- tabs:start -->

<!-- tab:Unicode -->

# 　

<span class="ErhaiLakeUI-icon" style="font-size: 100px; color: #80CEFF;">&#xe613;</span>

<!-- tab:Font class -->

# 　

<span class="ErhaiLakeUI-icon ErhaiLakeLogo" style="font-size: 100px; color: #80CEFF;"></span>

<!-- tab:Symbol -->

<svg class="svg-icon" aria-hidden="true" style="width: 100px; fill: #80CEFF;">
    <use xlink:href="#ErhaiLakeLogo"></use>
</svg>

<!-- tabs:end -->

<!-- tab:</> -->

<!-- tabs:start -->

<!-- tab:Unicode -->

```html
<span class="ErhaiLakeUI-icon" style="font-size: 100px; color: #80CEFF;">&#xe613;</span>
```

<!-- tab:Font class -->

```html
<span class="ErhaiLakeUI-icon ErhaiLakeLogo" style="font-size: 100px; color: #80CEFF;"></span>
```

<!-- tab:Symbol -->

```html
<svg class="svg-icon" aria-hidden="true" style="width: 100px; fill: #80CEFF;">
    <use xlink:href="#ErhaiLakeLogo"></use>
</svg>
```

<!-- tabs:end -->

<!-- tabs:end -->

## 各方法的优缺点

<!-- tabs:start -->

<!-- tab:Unicode -->

> Unicode 是字体在网页端最原始的应用方式,特点是:

- 支持按字体的方式去动态调整图标大小,颜色等等.
- 默认情况下不支持多色,直接添加多色图标会自动去色.

<!-- tab:Font class -->

> font-class 是 Unicode 使用方式的一种变种,主要是解决 Unicode 书写不直观,语意不明确的问题,与 Unicode 使用方式相比,具有如下特点:

- 相比于 Unicode 语意明确,书写更直观.可以很容易分辨这个 icon 是什么.
- 因为使用 class 来定义图标,所以当要替换图标时,只需要修改 class 里面的 Unicode 引用.

<!-- tab:Symbol -->

> 这是一种全新的使用方式,应该说这才是未来的主流,也是平台目前推荐的用法.,与另外两种相比具有如下特点:

- 支持多色图标了,不再受单色限制.
- 通过一些技巧,支持像字体那样,通过 font-size, color 来调整样式.
- 兼容性较差,支持 IE9+,及现代浏览器.
- 浏览器渲染 SVG 的性能一般,还不如 png.

<!-- tabs:end -->

## 使用方法

<!-- tabs:start -->

<!-- tab:Unicode -->

第一步:拷贝项目下面代码到你的项目中,图标库文件的路径要根据你的路径更改.

```css
@font-face {
  font-family: 'ErhaiLakeUI-icon';
  src: url('_media/fonts/ErhaiLakeUI-icon.woff2') format('woff2'),
       url('_media/fonts/ErhaiLakeUI-icon.woff') format('woff'),
       url('_media/fonts/ErhaiLakeUI-icon.ttf') format('truetype');
}
```

第二步:定义使用 ErhaiLakeUI 的样式,下面为例子:

```css
.ErhaiLakeUI-icon {
    font-family: "ErhaiLakeUI-icon" !important;
    font-size: 16px;
    font-style: normal;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
}
```

第三步:挑选相应图标并获取字体编码,应用于页面.

```html
<span class="ErhaiLakeUI-icon">&#x33;</span>
```

<!-- tab:Font class -->

第一步:引入 `ErhaiLakeUI.css` 到你的项目中.

```html
<link rel="stylesheet" href="/ErhailakeUI/ErhaiLakeUI/css/ErhaiLakeUI.css">
```

第二步:拷贝项目下面代码到你的项目中,图标库文件的路径要根据你的路径更改.

```css
@font-face {
  font-family: 'ErhaiLakeUI-icon';
  src: url('/ErhailakeUI/ErhaiLakeUI/fonts/ErhaiLakeUI-icon.woff2') format('woff2'),
       url('/ErhailakeUI/ErhaiLakeUI/fonts/ErhaiLakeUI-icon.woff') format('woff'),
       url('/ErhailakeUI/ErhaiLakeUI/fonts/ErhaiLakeUI-icon.ttf') format('truetype');
}
```

第二步:挑选相应图标并获取类名,应用于页面:

```html
<i class="ErhaiLakeUI-icon xxx"></i>
<span class="ErhaiLakeUI-icon xxx"></span>
```

<!-- tab:Symbol -->

第一步:引入 `ErhaiLakeUI.js` 到你的项目中.

```html
<script src="/ErhailakeUI/ErhaiLakeUI/js/ErhaiLakeUI.js"></script>
```

第二步:拷贝项目下面代码到你的项目中,图标库文件的路径要根据你的路径更改.

```css
@font-face {
  font-family: 'ErhaiLakeUI-icon';
  src: url('/ErhailakeUI/ErhaiLakeUI/fonts/ErhaiLakeUI-icon.woff2') format('woff2'),
       url('/ErhailakeUI/ErhaiLakeUI/fonts/ErhaiLakeUI-icon.woff') format('woff'),
       url('/ErhailakeUI/ErhaiLakeUI/fonts/ErhaiLakeUI-icon.ttf') format('truetype');
}
```

第三步:定义使用 ErhaiLakeUI 的样式,下面为例子:

```css
.ErhaiLakeUI-icon {
    width: 1em;
    height: 1em;
    vertical-align: -0.15em;
    fill: currentColor;
    overflow: hidden;
}
```

第四步:挑选相应图标并获取类名,应用于页面:

```html
<svg class="icon" aria-hidden="true">
    <use xlink:href="#icon-xxx"></use>
</svg>
```

<!-- tabs:end -->

目前收录了113个icon,如果有一些建议的icon,可以联系我,我会考虑丢进去的,然后将你加入贡献者名单!

## icon代码对照表

<!-- tabs:start -->

<!-- tab:Unicode -->

<div class="main">
    <div class="nav-tabs">
        <ul class="icon_lists dib-box">
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon">&#xe6a9;</span>
                <div class="name">报表</div>
                <div class="code-name">&amp;#xe6a9;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe6ac;</span>
              <div class="name">公告管理</div>
              <div class="code-name">&amp;#xe6ac;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe6ad;</span>
              <div class="name">活动</div>
              <div class="code-name">&amp;#xe6ad;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe6ae;</span>
              <div class="name">接口助手</div>
              <div class="code-name">&amp;#xe6ae;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe6af;</span>
              <div class="name">入驻管理</div>
              <div class="code-name">&amp;#xe6af;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe6b2;</span>
              <div class="name">系统组件</div>
              <div class="code-name">&amp;#xe6b2;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe6b5;</span>
              <div class="name">知识库</div>
              <div class="code-name">&amp;#xe6b5;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe6b6;</span>
              <div class="name">在线沟通</div>
              <div class="code-name">&amp;#xe6b6;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe6b7;</span>
              <div class="name">URL管理</div>
              <div class="code-name">&amp;#xe6b7;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe6bb;</span>
              <div class="name">错误</div>
              <div class="code-name">&amp;#xe6bb;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe6c2;</span>
              <div class="name">解绑</div>
              <div class="code-name">&amp;#xe6c2;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe6c4;</span>
              <div class="name">男</div>
              <div class="code-name">&amp;#xe6c4;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe6c5;</span>
              <div class="name">皮肤</div>
              <div class="code-name">&amp;#xe6c5;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe6c3;</span>
              <div class="name">控制台SQL</div>
              <div class="code-name">&amp;#xe6c3;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe6c6;</span>
              <div class="name">女</div>
              <div class="code-name">&amp;#xe6c6;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe6c7;</span>
              <div class="name">删除团队</div>
              <div class="code-name">&amp;#xe6c7;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe6c9;</span>
              <div class="name">添加团队</div>
              <div class="code-name">&amp;#xe6c9;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe6cc;</span>
              <div class="name">喜欢</div>
              <div class="code-name">&amp;#xe6cc;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe6cd;</span>
              <div class="name">文件夹视图</div>
              <div class="code-name">&amp;#xe6cd;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe6ce;</span>
              <div class="name">文件夹</div>
              <div class="code-name">&amp;#xe6ce;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe6cf;</span>
              <div class="name">新建文件夹</div>
              <div class="code-name">&amp;#xe6cf;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe6d5;</span>
              <div class="name">柱状图</div>
              <div class="code-name">&amp;#xe6d5;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe77f;</span>
              <div class="name">braces-fill</div>
              <div class="code-name">&amp;#xe77f;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe780;</span>
              <div class="name">brackets-fill</div>
              <div class="code-name">&amp;#xe780;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe781;</span>
              <div class="name">code-line</div>
              <div class="code-name">&amp;#xe781;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe782;</span>
              <div class="name">bug-fill</div>
              <div class="code-name">&amp;#xe782;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe783;</span>
              <div class="name">code-s-slash-line</div>
              <div class="code-name">&amp;#xe783;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe787;</span>
              <div class="name">terminal-box-line</div>
              <div class="code-name">&amp;#xe787;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe632;</span>
              <div class="name">语言</div>
              <div class="code-name">&amp;#xe632;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe63f;</span>
              <div class="name">复制</div>
              <div class="code-name">&amp;#xe63f;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe648;</span>
              <div class="name">买家发布需求</div>
              <div class="code-name">&amp;#xe648;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe6fa;</span>
              <div class="name">ok-ring</div>
              <div class="code-name">&amp;#xe6fa;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe6fb;</span>
              <div class="name">exclamation-point-ring</div>
              <div class="code-name">&amp;#xe6fb;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe6fc;</span>
              <div class="name">info-ring</div>
              <div class="code-name">&amp;#xe6fc;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe6fd;</span>
              <div class="name">close-ring</div>
              <div class="code-name">&amp;#xe6fd;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe6fe;</span>
              <div class="name">question-mark-ring</div>
              <div class="code-name">&amp;#xe6fe;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe629;</span>
              <div class="name">日志查询</div>
              <div class="code-name">&amp;#xe629;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe62a;</span>
              <div class="name">上一步</div>
              <div class="code-name">&amp;#xe62a;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe62b;</span>
              <div class="name">收起、减号</div>
              <div class="code-name">&amp;#xe62b;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe62c;</span>
              <div class="name">首页</div>
              <div class="code-name">&amp;#xe62c;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe62d;</span>
              <div class="name">添加、扩展</div>
              <div class="code-name">&amp;#xe62d;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe62e;</span>
              <div class="name">通行查询</div>
              <div class="code-name">&amp;#xe62e;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe62f;</span>
              <div class="name">未选择</div>
              <div class="code-name">&amp;#xe62f;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe630;</span>
              <div class="name">下一步</div>
              <div class="code-name">&amp;#xe630;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe631;</span>
              <div class="name">向下</div>
              <div class="code-name">&amp;#xe631;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe633;</span>
              <div class="name">向上</div>
              <div class="code-name">&amp;#xe633;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe634;</span>
              <div class="name">选中</div>
              <div class="code-name">&amp;#xe634;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe635;</span>
              <div class="name">用户编辑</div>
              <div class="code-name">&amp;#xe635;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe636;</span>
              <div class="name">用户信息</div>
              <div class="code-name">&amp;#xe636;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe637;</span>
              <div class="name">用户添加</div>
              <div class="code-name">&amp;#xe637;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe638;</span>
              <div class="name">用户授权</div>
              <div class="code-name">&amp;#xe638;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe639;</span>
              <div class="name">最后</div>
              <div class="code-name">&amp;#xe639;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe63a;</span>
              <div class="name">最前</div>
              <div class="code-name">&amp;#xe63a;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe63b;</span>
              <div class="name">我的异常</div>
              <div class="code-name">&amp;#xe63b;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe602;</span>
              <div class="name">c004邮件</div>
              <div class="code-name">&amp;#xe602;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe606;</span>
              <div class="name">c089退出</div>
              <div class="code-name">&amp;#xe606;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe848;</span>
              <div class="name">arrow-down箭头-下3</div>
              <div class="code-name">&amp;#xe848;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe849;</span>
              <div class="name">arrow-left-down箭头-左下</div>
              <div class="code-name">&amp;#xe849;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe84a;</span>
              <div class="name">arrow-right-top箭头-右上</div>
              <div class="code-name">&amp;#xe84a;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe84b;</span>
              <div class="name">arrow-top置顶</div>
              <div class="code-name">&amp;#xe84b;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe860;</span>
              <div class="name">日历</div>
              <div class="code-name">&amp;#xe860;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe862;</span>
              <div class="name">探索</div>
              <div class="code-name">&amp;#xe862;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe863;</span>
              <div class="name">数据2</div>
              <div class="code-name">&amp;#xe863;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe865;</span>
              <div class="name">压缩包</div>
              <div class="code-name">&amp;#xe865;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe866;</span>
              <div class="name">音频文件</div>
              <div class="code-name">&amp;#xe866;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe867;</span>
              <div class="name">预览2</div>
              <div class="code-name">&amp;#xe867;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe868;</span>
              <div class="name">注释</div>
              <div class="code-name">&amp;#xe868;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xeb94;</span>
              <div class="name">translate-2</div>
              <div class="code-name">&amp;#xeb94;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe600;</span>
              <div class="name">单选框-未选中</div>
              <div class="code-name">&amp;#xe600;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe601;</span>
              <div class="name">单选框-选中</div>
              <div class="code-name">&amp;#xe601;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe603;</span>
              <div class="name">对话框-成功</div>
              <div class="code-name">&amp;#xe603;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe604;</span>
              <div class="name">对话框-错误</div>
              <div class="code-name">&amp;#xe604;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe605;</span>
              <div class="name">对话框-警告</div>
              <div class="code-name">&amp;#xe605;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe607;</span>
              <div class="name">对话框-信息</div>
              <div class="code-name">&amp;#xe607;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe608;</span>
              <div class="name">对话框-询问</div>
              <div class="code-name">&amp;#xe608;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe609;</span>
              <div class="name">复选框-未选</div>
              <div class="code-name">&amp;#xe609;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe60a;</span>
              <div class="name">复选框-无效</div>
              <div class="code-name">&amp;#xe60a;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe60b;</span>
              <div class="name">复选框-选中</div>
              <div class="code-name">&amp;#xe60b;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe60c;</span>
              <div class="name">检测-二维码</div>
              <div class="code-name">&amp;#xe60c;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe60d;</span>
              <div class="name">检测-条形码</div>
              <div class="code-name">&amp;#xe60d;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe60e;</span>
              <div class="name">全部消息</div>
              <div class="code-name">&amp;#xe60e;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe60f;</span>
              <div class="name">218下载、导入备份@3x</div>
              <div class="code-name">&amp;#xe60f;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe610;</span>
              <div class="name">导出icon备份@3x</div>
              <div class="code-name">&amp;#xe610;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe611;</span>
              <div class="name">缓冲</div>
              <div class="code-name">&amp;#xe611;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe612;</span>
              <div class="name">加载</div>
              <div class="code-name">&amp;#xe612;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe614;</span>
              <div class="name">操作日志</div>
              <div class="code-name">&amp;#xe614;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe616;</span>
              <div class="name">账户管理</div>
              <div class="code-name">&amp;#xe616;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe613;</span>
              <div class="name">ErhaiLakeLogo</div>
              <div class="code-name">&amp;#xe613;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe624;</span>
              <div class="name">发送</div>
              <div class="code-name">&amp;#xe624;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe625;</span>
              <div class="name">编辑</div>
              <div class="code-name">&amp;#xe625;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe626;</span>
              <div class="name">附件</div>
              <div class="code-name">&amp;#xe626;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe627;</span>
              <div class="name">告警</div>
              <div class="code-name">&amp;#xe627;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe628;</span>
              <div class="name">购物</div>
              <div class="code-name">&amp;#xe628;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe63c;</span>
              <div class="name">可见</div>
              <div class="code-name">&amp;#xe63c;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe63d;</span>
              <div class="name">不可见</div>
              <div class="code-name">&amp;#xe63d;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe63e;</span>
              <div class="name">密码</div>
              <div class="code-name">&amp;#xe63e;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe640;</span>
              <div class="name">定位</div>
              <div class="code-name">&amp;#xe640;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe641;</span>
              <div class="name">时间</div>
              <div class="code-name">&amp;#xe641;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe642;</span>
              <div class="name">删除</div>
              <div class="code-name">&amp;#xe642;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe643;</span>
              <div class="name">视频</div>
              <div class="code-name">&amp;#xe643;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe644;</span>
              <div class="name">图片</div>
              <div class="code-name">&amp;#xe644;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe645;</span>
              <div class="name">收缩</div>
              <div class="code-name">&amp;#xe645;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe646;</span>
              <div class="name">搜索</div>
              <div class="code-name">&amp;#xe646;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe647;</span>
              <div class="name">登录</div>
              <div class="code-name">&amp;#xe647;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe649;</span>
              <div class="name">内容</div>
              <div class="code-name">&amp;#xe649;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe64a;</span>
              <div class="name">刷新</div>
              <div class="code-name">&amp;#xe64a;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe64b;</span>
              <div class="name">账号</div>
              <div class="code-name">&amp;#xe64b;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe64c;</span>
              <div class="name">筛选</div>
              <div class="code-name">&amp;#xe64c;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe64d;</span>
              <div class="name">文档</div>
              <div class="code-name">&amp;#xe64d;</div>
            </li>
            <li class="dib">
              <span class="icon ErhaiLakeUI-icon">&#xe64e;</span>
              <div class="name">展开</div>
              <div class="code-name">&amp;#xe64e;</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon">&#xe64f;</span>
                <div class="name">设置</div>
                <div class="code-name">&amp;#xe64f;</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon">&#xe650;</span>
                <div class="name">消息</div>
                <div class="code-name">&amp;#xe650;</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon">&#xe651;</span>
                <div class="name">完成</div>
                <div class="code-name">&amp;#xe651;</div>
            </li>
        </ul>
    </div>
</div>

<!-- tab:Font class -->

<div class="main">
    <div class="nav-tabs">
        <ul class="icon_lists dib-box">
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon baobiao"></span>
                <div class="name">报表</div>
                <div class="code-name">.baobiao</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon gonggaoguanli"></span>
                <div class="name">公告管理</div>
                <div class="code-name">.gonggaoguanli</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon huodong"></span>
                <div class="name">活动</div>
                <div class="code-name">.huodong</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon jiekouzhushou"></span>
                <div class="name">接口助手</div>
                <div class="code-name">.jiekouzhushou</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon ruzhuguanli"></span>
                <div class="name">入驻管理</div>
                <div class="code-name">.ruzhuguanli</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon xitongzujian"></span>
                <div class="name">系统组件</div>
                <div class="code-name">.xitongzujian</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon zhishiku"></span>
                <div class="name">知识库</div>
                <div class="code-name">.zhishiku</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon zaixiangoutong"></span>
                <div class="name">在线沟通
                </div>
                <div class="code-name">.zaixiangoutong
                </div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon URLguanli"></span>
                <div class="name">URL管理</div>
                <div class="code-name">.URLguanli</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon cuowu"></span>
                <div class="name">错误</div>
                <div class="code-name">.cuowu</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon jiebang"></span>
                <div class="name">解绑</div>
                <div class="code-name">.jiebang</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon nan"></span>
                <div class="name">男</div>
                <div class="code-name">.nan</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon pifu"></span>
                <div class="name">皮肤</div>
                <div class="code-name">.pifu</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon kongzhitaiSQL"></span>
                <div class="name">控制台SQL</div>
                <div class="code-name">.kongzhitaiSQL</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon nv"></span>
                <div class="name">女</div>
                <div class="code-name">.nv</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon shanchutuandui"></span>
                <div class="name">删除团队</div>
                <div class="code-name">.shanchutuandui</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon tianjiatuandui"></span>
                <div class="name">添加团队</div>
                <div class="code-name">.tianjiatuandui</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon xihuan"></span>
                <div class="name">喜欢</div>
                <div class="code-name">.xihuan</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon wenjianjiashitu"></span>
                <div class="name">文件夹视图</div>
                <div class="code-name">.wenjianjiashitu</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon wenjianjia"></span>
                <div class="name">文件夹</div>
                <div class="code-name">.wenjianjia</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon xinjianwenjianjia"></span>
                <div class="name">新建文件夹</div>
                <div class="code-name">.xinjianwenjianjia</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon zhuzhuangtu"></span>
                <div class="name">柱状图</div>
                <div class="code-name">.zhuzhuangtu</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon braces-fill"></span>
                <div class="name">braces-fill</div>
                <div class="code-name">.braces-fill</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon brackets-fill"></span>
                <div class="name">brackets-fill</div>
                <div class="code-name">.brackets-fill</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon code-line"></span>
                <div class="name">code-line</div>
                <div class="code-name">.code-line</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon bug-fill"></span>
                <div class="name">bug-fill</div>
                <div class="code-name">.bug-fill</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon code-s-slash-line"></span>
                <div class="name">code-s-slash-line</div>
                <div class="code-name">.code-s-slash-line</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon terminal-box-line"></span>
                <div class="name">terminal-box-line</div>
                <div class="code-name">.terminal-box-line</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon ditu"></span>
                <div class="name">语言</div>
                <div class="code-name">.ditu</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon fuzhi"></span>
                <div class="name">复制</div>
                <div class="code-name">.fuzhi</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon maijiafabuxuqiu"></span>
                <div class="name">买家发布需求</div>
                <div class="code-name">.maijiafabuxuqiu</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon ok-ring"></span>
                <div class="name">ok-ring</div>
                <div class="code-name">.ok-ring</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon exclamation-point-ring"></span>
                <div class="name">exclamation-point-ring</div>
                <div class="code-name">.exclamation-point-ring</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon info-ring"></span>
                <div class="name">info-ring</div>
                <div class="code-name">.info-ring</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon close-ring"></span>
                <div class="name">close-ring</div>
                <div class="code-name">.close-ring</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon question-mark-ring"></span>
                <div class="name">question-mark-ring</div>
                <div class="code-name">.question-mark-ring</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon rizhichaxun"></span>
                <div class="name">日志查询</div>
                <div class="code-name">.rizhichaxun</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon shangyibu"></span>
                <div class="name">上一步</div>
                <div class="code-name">.shangyibu</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon a-shouqijianhao"></span>
                <div class="name">收起、减号</div>
                <div class="code-name">.a-shouqijianhao</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon shouye"></span>
                <div class="name">首页</div>
                <div class="code-name">.shouye</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon a-tianjiakuozhan"></span>
                <div class="name">添加、扩展</div>
                <div class="code-name">.a-tianjiakuozhan</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon tonghangchaxun"></span>
                <div class="name">通行查询</div>
                <div class="code-name">.tonghangchaxun</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon weixuanze"></span>
                <div class="name">未选择</div>
                <div class="code-name">.weixuanze</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon xiayibu"></span>
                <div class="name">下一步</div>
                <div class="code-name">.xiayibu</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon xiangxia"></span>
                <div class="name">向下</div>
                <div class="code-name">.xiangxia</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon xiangshang"></span>
                <div class="name">向上</div>
                <div class="code-name">.xiangshang</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon xuanzhong"></span>
                <div class="name">选中</div>
                <div class="code-name">.xuanzhong</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon yonghubianji"></span>
                <div class="name">用户编辑</div>
                <div class="code-name">.yonghubianji</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon yonghuxinxi"></span>
                <div class="name">用户信息</div>
                <div class="code-name">.yonghuxinxi</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon yonghutianjia"></span>
                <div class="name">用户添加</div>
                <div class="code-name">.yonghutianjia</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon yonghushouquan"></span>
                <div class="name">用户授权</div>
                <div class="code-name">.yonghushouquan</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon zuihou"></span>
                <div class="name">最后</div>
                <div class="code-name">.zuihou</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon zuiqian"></span>
                <div class="name">最前</div>
                <div class="code-name">.zuiqian</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon wdyc-copy"></span>
                <div class="name">我的异常</div>
                <div class="code-name">.wdyc-copy</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon c004youjian"></span>
                <div class="name">c004邮件</div>
                <div class="code-name">.c004youjian</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon c089tuichu"></span>
                <div class="name">c089退出</div>
                <div class="code-name">.c089tuichu</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon arrow-downjiantou-xia3"></span>
                <div class="name">arrow-down箭头-下3</div>
                <div class="code-name">.arrow-downjiantou-xia3</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon arrow-left-downjiantou-zuoxia"></span>
                <div class="name">arrow-left-down箭头-左下</div>
                <div class="code-name">.arrow-left-downjiantou-zuoxia</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon arrow-right-topjiantou-youshang"></span>
                <div class="name">arrow-right-top箭头-右上</div>
                <div class="code-name">.arrow-right-topjiantou-youshang</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon arrow-topzhiding"></span>
                <div class="name">arrow-top置顶</div>
                <div class="code-name">.arrow-topzhiding</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon rili"></span>
                <div class="name">日历</div>
                <div class="code-name">.rili</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon tansuo"></span>
                <div class="name">探索</div>
                <div class="code-name">.tansuo</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon shuju2"></span>
                <div class="name">数据2</div>
                <div class="code-name">.shuju2</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon yasuobao"></span>
                <div class="name">压缩包</div>
                <div class="code-name">.yasuobao</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon yinpinwenjian"></span>
                <div class="name">音频文件</div>
                <div class="code-name">.yinpinwenjian</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon yulan2"></span>
                <div class="name">预览2</div>
                <div class="code-name">.yulan2</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon zhushi"></span>
                <div class="name">注释</div>
                <div class="code-name">.zhushi</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon translate-2"></span>
                <div class="name">translate-2</div>
                <div class="code-name">.translate-2</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon danxuankuang-weixuanzhong"></span>
                <div class="name">单选框-未选中</div>
                <div class="code-name">.danxuankuang-weixuanzhong</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon danxuankuang-xuanzhong"></span>
                <div class="name">单选框-选中</div>
                <div class="code-name">.danxuankuang-xuanzhong</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon duihuakuang-chenggong"></span>
                <div class="name">对话框-成功</div>
                <div class="code-name">.duihuakuang-chenggong</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon duihuakuang-cuowu"></span>
                <div class="name">对话框-错误</div>
                <div class="code-name">.duihuakuang-cuowu</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon duihuakuang-jinggao"></span>
                <div class="name">对话框-警告</div>
                <div class="code-name">.duihuakuang-jinggao</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon duihuakuang-xinxi"></span>
                <div class="name">对话框-信息</div>
                <div class="code-name">.duihuakuang-xinxi</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon duihuakuang-xunwen"></span>
                <div class="name">对话框-询问</div>
                <div class="code-name">.duihuakuang-xunwen</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon fuxuankuang-weixuan"></span>
                <div class="name">复选框-未选</div>
                <div class="code-name">.fuxuankuang-weixuan</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon fuxuankuang-wuxiao"></span>
                <div class="name">复选框-无效</div>
                <div class="code-name">.fuxuankuang-wuxiao</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon fuxuankuang-xuanzhong"></span>
                <div class="name">复选框-选中</div>
                <div class="code-name">.fuxuankuang-xuanzhong</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon jiance-erweima"></span>
                <div class="name">检测-二维码</div>
                <div class="code-name">.jiance-erweima</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon jiance-tiaoxingma"></span>
                <div class="name">检测-条形码</div>
                <div class="code-name">.jiance-tiaoxingma</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon a-quanbuxiaoxiiconbeifen3x"></span>
                <div class="name">全部消息</div>
                <div class="code-name">.a-quanbuxiaoxiiconbeifen3x</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon a-218xiazaidaorubeifen3x"></span>
                <div class="name">218下载、导入备份@3x</div>
                <div class="code-name">.a-218xiazaidaorubeifen3x</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon a-daochuiconbeifen3x"></span>
                <div class="name">导出icon备份@3x</div>
                <div class="code-name">.a-daochuiconbeifen3x</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon sync"></span>
                <div class="name">缓冲</div>
                <div class="code-name">.sync</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon reload"></span>
                <div class="name">加载</div>
                <div class="code-name">.reload</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon a-caozuorizhi3x"></span>
                <div class="name">操作日志</div>
                <div class="code-name">.a-caozuorizhi3x</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon a-1"></span>
                <div class="name">账户管理</div>
                <div class="code-name">.a-1</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon ErhaiLakeLogo"></span>
                <div class="name">ErhaiLakeLogo</div>
                <div class="code-name">.ErhaiLakeLogo</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon fasong"></span>
                <div class="name">发送</div>
                <div class="code-name">.fasong</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon bianji"></span>
                <div class="name">编辑</div>
                <div class="code-name">.bianji</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon fujian"></span>
                <div class="name">附件</div>
                <div class="code-name">.fujian</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon gaojing"></span>
                <div class="name">告警</div>
                <div class="code-name">.gaojing</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon gouwu"></span>
                <div class="name">购物</div>
                <div class="code-name">.gouwu</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon kejian"></span>
                <div class="name">可见</div>
                <div class="code-name">.kejian</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon bukejian"></span>
                <div class="name">不可见</div>
                <div class="code-name">.bukejian</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon mima"></span>
                <div class="name">密码</div>
                <div class="code-name">.mima</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon dingwei"></span>
                <div class="name">定位</div>
                <div class="code-name">.dingwei</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon shijian"></span>
                <div class="name">时间</div>
                <div class="code-name">.shijian</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon shanchu"></span>
                <div class="name">删除</div>
                <div class="code-name">.shanchu</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon shipin"></span>
                <div class="name">视频</div>
                <div class="code-name">.shipin</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon tupian"></span>
                <div class="name">图片</div>
                <div class="code-name">.tupian</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon shousuo"></span>
                <div class="name">收缩</div>
                <div class="code-name">.shousuo</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon sousuo"></span>
                <div class="name">搜索</div>
                <div class="code-name">.sousuo</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon denglu"></span>
                <div class="name">登录</div>
                <div class="code-name">.denglu</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon neirong"></span>
                <div class="name">内容</div>
                <div class="code-name">.neirong</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon shuaxin"></span>
                <div class="name">刷新</div>
                <div class="code-name">.shuaxin</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon zhanghao"></span>
                <div class="name">账号</div>
                <div class="code-name">.zhanghao</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon shaixuan"></span>
                <div class="name">筛选</div>
                <div class="code-name">.shaixuan</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon wendang"></span>
                <div class="name">文档</div>
                <div class="code-name">.wendang</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon zhankai"></span>
                <div class="name">展开</div>
                <div class="code-name">.zhankai</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon shezhi"></span>
                <div class="name">设置</div>
                <div class="code-name">.shezhi</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon xiaoxi"></span>
                <div class="name">消息</div>
                <div class="code-name">.xiaoxi</div>
            </li>
            <li class="dib">
                <span class="icon ErhaiLakeUI-icon wancheng"></span>
                <div class="name">完成</div>
                <div class="code-name">.wancheng</div>
            </li>
        </ul>
    </div>
</div>

<!-- tab:Symbol -->

<div class="main">
    <div class="nav-tabs">
        <ul class="icon_lists dib-box">
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#baobiao"></use></svg>
                <div class="name">报表</div>
                <div class="code-name">#baobiao</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#gonggaoguanli"></use></svg>
                <div class="name">公告管理</div>
                <div class="code-name">#gonggaoguanli</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#huodong"></use></svg>
                <div class="name">活动</div>
                <div class="code-name">#huodong</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#jiekouzhushou"></use></svg>
                <div class="name">接口助手</div>
                <div class="code-name">#jiekouzhushou</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#ruzhuguanli"></use></svg>
                <div class="name">入驻管理</div>
                <div class="code-name">#ruzhuguanli</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#xitongzujian"></use></svg>
                <div class="name">系统组件</div>
                <div class="code-name">#xitongzujian</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#zhishiku"></use></svg>
                <div class="name">知识库</div>
                <div class="code-name">#zhishiku</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#zaixiangoutong"></use></svg>
                <div class="name">在线沟通</div>
                <div class="code-name">#zaixiangoutong</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#URLguanli"></use></svg>
                <div class="name">URL管理</div>
                <div class="code-name">#URLguanli</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#cuowu"></use></svg>
                <div class="name">错误</div>
                <div class="code-name">#cuowu</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#jiebang"></use></svg>
                <div class="name">解绑</div>
                <div class="code-name">#jiebang</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#nan"></use></svg>
                <div class="name">男</div>
                <div class="code-name">#nan</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#pifu"></use></svg>
                <div class="name">皮肤</div>
                <div class="code-name">#pifu</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#kongzhitaiSQL"></use></svg>
                <div class="name">控制台SQL</div>
                <div class="code-name">#kongzhitaiSQL</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#nv"></use></svg>
                <div class="name">女</div>
                <div class="code-name">#nv</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#shanchutuandui"></use></svg>
                <div class="name">删除团队</div>
                <div class="code-name">#shanchutuandui</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#tianjiatuandui"></use></svg>
                <div class="name">添加团队</div>
                <div class="code-name">#tianjiatuandui</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#xihuan"></use></svg>
                <div class="name">喜欢</div>
                <div class="code-name">#xihuan</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#wenjianjiashitu"></use></svg>
                <div class="name">文件夹视图</div>
                <div class="code-name">#wenjianjiashitu</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#wenjianjia"></use></svg>
                <div class="name">文件夹</div>
                <div class="code-name">#wenjianjia</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#xinjianwenjianjia"></use></svg>
                <div class="name">新建文件夹</div>
                <div class="code-name">#xinjianwenjianjia</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#zhuzhuangtu"></use></svg>
                <div class="name">柱状图</div>
                <div class="code-name">#zhuzhuangtu</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#braces-fill"></use></svg>
                <div class="name">braces-fill</div>
                <div class="code-name">#braces-fill</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#brackets-fill"></use></svg>
                <div class="name">brackets-fill</div>
                <div class="code-name">#brackets-fill</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#code-line"></use></svg>
                <div class="name">code-line</div>
                <div class="code-name">#code-line</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#bug-fill"></use></svg>
                <div class="name">bug-fill</div>
                <div class="code-name">#bug-fill</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#code-s-slash-line"></use></svg>
                <div class="name">code-s-slash-line</div>
                <div class="code-name">#code-s-slash-line</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#terminal-box-line"></use></svg>
                <div class="name">terminal-box-line</div>
                <div class="code-name">#terminal-box-line</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#ditu"></use></svg>
                <div class="name">语言</div>
                <div class="code-name">#ditu</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#fuzhi"></use></svg>
                <div class="name">复制</div>
                <div class="code-name">#fuzhi</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#maijiafabuxuqiu"></use></svg>
                <div class="name">买家发布需求</div>
                <div class="code-name">#maijiafabuxuqiu</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#ok-ring"></use></svg>
                <div class="name">ok-ring</div>
                <div class="code-name">#ok-ring</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#exclamation-point-ring"></use></svg>
                <div class="name">exclamation-point-ring</div>
                <div class="code-name">#exclamation-point-ring</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#info-ring"></use></svg>
                <div class="name">info-ring</div>
                <div class="code-name">#info-ring</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#close-ring"></use></svg>
                <div class="name">close-ring</div>
                <div class="code-name">#close-ring</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#question-mark-ring"></use></svg>
                <div class="name">question-mark-ring</div>
                <div class="code-name">#question-mark-ring</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#rizhichaxun"></use></svg>
                <div class="name">日志查询</div>
                <div class="code-name">#rizhichaxun</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#shangyibu"></use></svg>
                <div class="name">上一步</div>
                <div class="code-name">#shangyibu</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#a-shouqijianhao"></use></svg>
                <div class="name">收起、减号</div>
                <div class="code-name">#a-shouqijianhao</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#shouye"></use></svg>
                <div class="name">首页</div>
                <div class="code-name">#shouye</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#a-tianjiakuozhan"></use></svg>
                <div class="name">添加、扩展</div>
                <div class="code-name">#a-tianjiakuozhan</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#tonghangchaxun"></use></svg>
                <div class="name">通行查询</div>
                <div class="code-name">#tonghangchaxun</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#weixuanze"></use></svg>
                <div class="name">未选择</div>
                <div class="code-name">#weixuanze</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#xiayibu"></use></svg>
                <div class="name">下一步</div>
                <div class="code-name">#xiayibu</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#xiangxia"></use></svg>
                <div class="name">向下</div>
                <div class="code-name">#xiangxia</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#xiangshang"></use></svg>
                <div class="name">向上</div>
                <div class="code-name">#xiangshang</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#xuanzhong"></use></svg>
                <div class="name">选中</div>
                <div class="code-name">#xuanzhong</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#yonghubianji"></use></svg>
                <div class="name">用户编辑</div>
                <div class="code-name">#yonghubianji</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#yonghuxinxi"></use></svg>
                <div class="name">用户信息</div>
                <div class="code-name">#yonghuxinxi</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#yonghutianjia"></use></svg>
                <div class="name">用户添加</div>
                <div class="code-name">#yonghutianjia</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#yonghushouquan"></use></svg>
                <div class="name">用户授权</div>
                <div class="code-name">#yonghushouquan</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#zuihou"></use></svg>
                <div class="name">最后</div>
                <div class="code-name">#zuihou</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#zuiqian"></use></svg>
                <div class="name">最前</div>
                <div class="code-name">#zuiqian</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#wdyc-copy"></use></svg>
                <div class="name">我的异常</div>
                <div class="code-name">#wdyc-copy</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#c004youjian"></use></svg>
                <div class="name">c004邮件</div>
                <div class="code-name">#c004youjian</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#c089tuichu"></use></svg>
                <div class="name">c089退出</div>
                <div class="code-name">#c089tuichu</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#arrow-downjiantou-xia3"></use></svg>
                <div class="name">arrow-down箭头-下3</div>
                <div class="code-name">#arrow-downjiantou-xia3</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#arrow-left-downjiantou-zuoxia"></use></svg>
                <div class="name">arrow-left-down箭头-左下</div>
                <div class="code-name">#arrow-left-downjiantou-zuoxia</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#arrow-right-topjiantou-youshang"></use></svg>
                <div class="name">arrow-right-top箭头-右上</div>
                <div class="code-name">#arrow-right-topjiantou-youshang</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#arrow-topzhiding"></use></svg>
                <div class="name">arrow-top置顶</div>
                <div class="code-name">#arrow-topzhiding</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#rili"></use></svg>
                <div class="name">日历</div>
                <div class="code-name">#rili</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#tansuo"></use></svg>
                <div class="name">探索</div>
                <div class="code-name">#tansuo</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#shuju2"></use></svg>
                <div class="name">数据2</div>
                <div class="code-name">#shuju2</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#yasuobao"></use></svg>
                <div class="name">压缩包</div>
                <div class="code-name">#yasuobao</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#yinpinwenjian"></use></svg>
                <div class="name">音频文件</div>
                <div class="code-name">#yinpinwenjian</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#yulan2"></use></svg>
                <div class="name">预览2</div>
                <div class="code-name">#yulan2</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#zhushi"></use></svg>
                <div class="name">注释</div>
                <div class="code-name">#zhushi</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#translate-2"></use></svg>
                <div class="name">translate-2</div>
                <div class="code-name">#translate-2</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#danxuankuang-weixuanzhong"></use></svg>
                <div class="name">单选框-未选中</div>
                <div class="code-name">#danxuankuang-weixuanzhong</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#danxuankuang-xuanzhong"></use></svg>
                <div class="name">单选框-选中</div>
                <div class="code-name">#danxuankuang-xuanzhong</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#duihuakuang-chenggong"></use></svg>
                <div class="name">对话框-成功</div>
                <div class="code-name">#duihuakuang-chenggong</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#duihuakuang-cuowu"></use></svg>
                <div class="name">对话框-错误</div>
                <div class="code-name">#duihuakuang-cuowu</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#duihuakuang-jinggao"></use></svg>
                <div class="name">对话框-警告</div>
                <div class="code-name">#duihuakuang-jinggao</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#duihuakuang-xinxi"></use></svg>
                <div class="name">对话框-信息</div>
                <div class="code-name">#duihuakuang-xinxi</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#duihuakuang-xunwen"></use></svg>
                <div class="name">对话框-询问</div>
                <div class="code-name">#duihuakuang-xunwen</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#fuxuankuang-weixuan"></use></svg>
                <div class="name">复选框-未选</div>
                <div class="code-name">#fuxuankuang-weixuan</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#fuxuankuang-wuxiao"></use></svg>
                <div class="name">复选框-无效</div>
                <div class="code-name">#fuxuankuang-wuxiao</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#fuxuankuang-xuanzhong"></use></svg>
                <div class="name">复选框-选中</div>
                <div class="code-name">#fuxuankuang-xuanzhong</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#jiance-erweima"></use></svg>
                <div class="name">检测-二维码</div>
                <div class="code-name">#jiance-erweima</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#jiance-tiaoxingma"></use></svg>
                <div class="name">检测-条形码</div>
                <div class="code-name">#jiance-tiaoxingma</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#a-quanbuxiaoxiiconbeifen3x"></use></svg>
                <div class="name">全部消息</div>
                <div class="code-name">#a-quanbuxiaoxiiconbeifen3x</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#a-218xiazaidaorubeifen3x"></use></svg>
                <div class="name">218下载、导入备份@3x</div>
                <div class="code-name">#a-218xiazaidaorubeifen3x</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#a-daochuiconbeifen3x"></use></svg>
                <div class="name">导出icon备份@3x</div>
                <div class="code-name">#a-daochuiconbeifen3x</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#sync"></use></svg>
                <div class="name">缓冲</div>
                <div class="code-name">#sync</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#reload"></use></svg>
                <div class="name">加载</div>
                <div class="code-name">#reload</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#a-caozuorizhi3x"></use></svg>
                <div class="name">操作日志</div>
                <div class="code-name">#a-caozuorizhi3x</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#a-1"></use></svg>
                <div class="name">账户管理</div>
                <div class="code-name">#a-1</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#ErhaiLakeLogo"></use></svg>
                <div class="name">ErhaiLakeLogo</div>
                <div class="code-name">#ErhaiLakeLogo</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#fasong"></use></svg>
                <div class="name">发送</div>
                <div class="code-name">#fasong</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#bianji"></use></svg>
                <div class="name">编辑</div>
                <div class="code-name">#bianji</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#fujian"></use></svg>
                <div class="name">附件</div>
                <div class="code-name">#fujian</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#gaojing"></use></svg>
                <div class="name">告警</div>
                <div class="code-name">#gaojing</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#gouwu"></use></svg>
                <div class="name">购物</div>
                <div class="code-name">#gouwu</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#kejian"></use></svg>
                <div class="name">可见</div>
                <div class="code-name">#kejian</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#bukejian"></use></svg>
                <div class="name">不可见</div>
                <div class="code-name">#bukejian</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#mima"></use></svg>
                <div class="name">密码</div>
                <div class="code-name">#mima</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#dingwei"></use></svg>
                <div class="name">定位</div>
                <div class="code-name">#dingwei</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#shijian"></use></svg>
                <div class="name">时间</div>
                <div class="code-name">#shijian</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#shanchu"></use></svg>
                <div class="name">删除</div>
                <div class="code-name">#shanchu</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#shipin"></use></svg>
                <div class="name">视频</div>
                <div class="code-name">#shipin</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#tupian"></use></svg>
                <div class="name">图片</div>
                <div class="code-name">#tupian</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#shousuo"></use></svg>
                <div class="name">收缩</div>
                <div class="code-name">#shousuo</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#sousuo"></use></svg>
                <div class="name">搜索</div>
                <div class="code-name">#sousuo</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#denglu"></use></svg>
                <div class="name">登录</div>
                <div class="code-name">#denglu</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#neirong"></use></svg>
                <div class="name">内容</div>
                <div class="code-name">#neirong</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#shuaxin"></use></svg>
                <div class="name">刷新</div>
                <div class="code-name">#shuaxin</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#zhanghao"></use></svg>
                <div class="name">账号</div>
                <div class="code-name">#zhanghao</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#shaixuan"></use></svg>
                <div class="name">筛选</div>
                <div class="code-name">#shaixuan</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#wendang"></use></svg>
                <div class="name">文档</div>
                <div class="code-name">#wendang</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#zhankai"></use></svg>
                <div class="name">展开</div>
                <div class="code-name">#zhankai</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#shezhi"></use></svg>
                <div class="name">设置</div>
                <div class="code-name">#shezhi</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#xiaoxi"></use></svg>
                <div class="name">消息</div>
                <div class="code-name">#xiaoxi</div>
            </li>
            <li class="dib">
                <svg class="icon svg-icon" aria-hidden="true"><use xlink:href="#wancheng"></use></svg>
                <div class="name">完成</div>
                <div class="code-name">#wancheng</div>
            </li>
        </ul>
    </div>
</div>

<!-- tabs:end -->