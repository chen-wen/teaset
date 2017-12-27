# `<Popover />` 气泡
Popover 组件定义一个气泡, 是一个可在边框任意位置显示一个三角形箭头的圆角矩形容器, 常用于聊天信息显示或弹出提示等。

## Props
| Prop | Type | Default | Note |
|---|---|---|---|
| [View props...](https://facebook.github.io/react-native/docs/view.html) |  |  | Popover 组件继承 View 组件的全部属性。
| arrow | string | 'none' | 三角形箭头的位置。<br/>- none: 无<br/>- topLeft: 上边左侧<br/>- top: 上边居中<br/>- topRight: 上边右侧<br/>- rightTop: 右边上侧<br/>- right: 右边居中<br/>- rightBottom: 右边下侧<br/>- bottomRight: 下边右侧<br/>- bottom: 下边居中<br/>- bottomLeft: 下边左侧<br/>- leftBottom: 左边下侧<br/>- left: 左边居中<br/>- leftTop: 左边上侧<br/>显示效果参见[Screenshots](#screenshots)。
| paddingCorner | number |  | 三角形箭头与角点距离, 与 arrow 值有关, 如 arrow = 'topLeft' 时表示三角形箭头与左上角的距离, 默认值在 Theme 中设置。

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
<Popover arrow='bottom'>
  <Label text='Popover' />
</Popover>
```

自定义
```
let blackStyle = {
  backgroundColor: 'rgba(0, 0, 0, 0.8)',
  paddingTop: 8,
  paddingBottom: 8,
  paddingLeft: 12,
  paddingRight: 12,
};
let shadowStyle = {
  shadowColor: '#777',
  shadowOffset: {width: 1, height: 1},
  shadowOpacity: 0.5,
  shadowRadius: 2,
};

...

<Popover style={[blackStyle, shadowStyle]} arrow='topLeft' paddingCorner={16}>
  <Label text='Popover' />
</Popover>
```


## Screenshots
![](https://github.com/rilyu/teaset/blob/master/screenshots/07-Popover.png?raw=true)


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