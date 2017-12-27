# `ModalIndicator{}` 模态指示器
ModalIndicator 为模态指示器静态类, 一般在需要阻止用户操作时使用, 比如提交数据等, 表现形式为一个覆盖全屏的模态指示器。<br/>ModalIndicator 基于 [Overlay{}](./Overlay.md) 实现。

## Static Methods
| Method | Params | Returns | Notes |
|---|---|---|---|
| [Overlay methods](./Overlay.md) |  |  | ModalIndicator 继承 Overlay 的全部静态方法。
| show | text | key | 弹出模态指示器, 重写 [Overlay{}](./Overlay.md) 中的同名函数, 输入参数 text 为模态指示器下显示的文本，如调用此函数前已显示模态指示器则仅更换文本。
| hide |  |  | 隐藏模态指示器。

## Static Props
| Prop | Type | Default | Note |
|---|---|---|---|
| [IndicatorView](#modalindicatorindicatorview--props) | class |  | ModalIndicator 内容显示组件。

## `<ModalIndicator.IndicatorView />` Props
| Prop | Type | Default | Note |
|---|---|---|---|
| [View props...](https://facebook.github.io/react-native/docs/view.html) |  |  | ModalIndicator.IndicatorView 组件继承 View 组件的全部属性。
| text | string<br/>number<br/>element |  | 文本, 可以是字符串、数字或 React Native 组件。
| position | string | 'center' | 模态指示器显示位置。<br/>- top: 窗口靠上位置<br/>- bottom: 窗口靠下位置<br/>- center: 窗口中间位置<br/>top 、 bottom 位置可在 Theme 中设置。
| size | 同ActivityIndicator.size | 'large' | 模态指示器大小。
| color | 同ActivityIndicator.color |  | 模态指示器颜色, 默认值在 Theme 中设置。

## Example
简单用法
```
ModalIndicator.show(`Modal indicator`);
```


## Screenshots
![](https://github.com/rilyu/teaset/blob/master/screenshots/21-ModalIndicator.png?raw=true)


<div class="sidebar">
<dl>
    <dt>主题</dt>
    <dd><a href="./Theme.html">Theme|主题</a></dd>
</dl> 
<dl>
    <dt>基础组件</dt>
    <dd><a href="./Label.html">Label|标签</a></dd>
    <dd><a href="./Button.html">Button|按钮</a></dd>
    <dd><a href="./Checkbox.html">Checkbox|复选框</a></dd>
    <dd><a href="./Input.html">Input|输入框</a></dd>
    <dd><a href="./Select.html">Select|选择框</a></dd>
    <dd><a href="./Stepper.html">Stepper|步进器</a></dd>
    <dd><a href="./SearchInput.html">SearchInput|搜索输入框</a></dd>
    <dd><a href="./Badge.html">Badge|徽章</a></dd>
    <dd><a href="./Popover.html">Popover|气泡</a></dd>
</dl> 
<dl>
    <dt>复合组件</dt>
    <dd><a href="./NavigationBar.html">NavigationBar|导航栏</a></dd>
    <dd><a href="./ListRow.html">ListRow|列表行</a></dd>
    <dd><a href="./Carousel.html">Carousel|走马灯</a></dd>
    <dd><a href="./Projector.html">Projector|幻灯机</a></dd>
    <dd><a href="./SegmentedBar.html">SegmentedBar|分段工具条</a></dd>
    <dd><a href="./SegmentedView.html">SegmentedView|分段器</a></dd>
    <dd><a href="./TabView.html">TabView|标签页</a></dd>
    <dd><a href="./TransformView.html">TransformView|可变视图</a></dd>
    <dd><a href="./AlbumView.html">AlbumView|相册视图</a></dd>
    <dd><a href="./Wheel.html">Wheel|滚轮</a></dd>
</dl> 
<dl>
    <dt>浮层</dt>
    <dd><a href="./Overlay.html">Overlay|浮层</a></dd>
    <dd><a href="./Toast.html">Toast|轻提示</a></dd>
    <dd><a href="./ActionSheet.html">ActionSheet|操作选单</a></dd>
    <dd><a href="./ActionPopover.html">ActionPopover|操作气泡</a></dd>
    <dd><a href="./PullPicker.html">PullPicker|上拉选择器</a></dd>
    <dd><a href="./PopoverPicker.html">PopoverPicker|气泡选择器</a></dd>
    <dd><a href="./Menu.html">Menu|菜单</a></dd>
    <dd><a href="./Drawer.html">Drawer|抽屉</a></dd>
    <dd><a href="./ModalIndicator.html">ModalIndicator|模态指示器</a></dd>
</dl> 
<dl>
    <dt>页面</dt>
    <dd><a href="./TeaNavigator.html">TeaNavigator|导航器</a></dd>
    <dd><a href="./BasePage.html">BasePage|基础页面</a></dd>
    <dd><a href="./NavigationPage.html">NavigationPage|导航页面</a></dd>
</dl> 
</div>
<style>
    .sidebar{
      position:fixed;
      right:0px;
      top:0;
      background:#efefef;
      padding:0 15px;
      width: 220px;
      height:100%;
      overflow-y:scroll;
    }
    .sidebar dl dd{
        margin-bottom: 0;
    }
    .sidebar a {
        font-size: 12px;
    }
    .container-lg {
        margin-right: 230px;
    }
</style>