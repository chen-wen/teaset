# `<Label />` 标签
Label 组件用于文本显示, 一般为单行的少量文字。

## Props
| Prop | Type | Default | Note |
|---|---|---|---|
| [Text props...](https://facebook.github.io/react-native/docs/text.html) |  |  | Label 组件继承 Text 组件的全部属性。
| type | string | 'default' | 显示样式类型。<br/>- default: 在默认 Theme 中定义的字体颜色为深灰色(#333)<br/>- title: 在默认 Theme 中定义的字体颜色为黑色(#000), 字体大小为 default 的 1.1 倍<br/>- detail: 在默认 Theme 中定义的字体颜色为浅灰色(#989898), 字体大小为 default 的 0.9 倍<br/>- danger: 在默认 Theme 中定义的字体颜色为红色(#a94442)<br>显示效果参见[Screenshots](#screenshots)。
| size | string | 'md' | 显示尺寸大小。<br/>- xl: 超大, 在默认 Theme 中定义的字体大小为 26<br/>- lg: 大, 在默认 Theme 中定义的字体大小为 20<br/>- md: 中, 在默认 Theme 中定义的字体大小为 14<br/>- sm: 小, 在默认 Theme 中定义的字体大小为 10<br/>- xs: 超小, 在默认 Theme 中定义的字体大小为 8<br>显示效果参见[Screenshots](#screenshots)。
| text | string<br/>number |  | 显示文本, 可以是字符串或数字。
| numberOfLines | number | 1 | 显示行数, 继承自 Text 组件并修改默认值。

<!--
## Events
None.

## Methods
None.

## Static Props
None.

## Static Methods
None.
-->

## Example
简单用法
```
<Label text='Hello world' />
```

使用 type、size 属性
```
<Label type='title' size='xl' text='Hello world' />
```

自定义 style
```
<Label style={{color: '#8a6d3b', fontSize: 16}} text='Hello world' />
```

## Screenshots
![](https://github.com/rilyu/teaset/blob/master/screenshots/01-Label.png?raw=true)



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