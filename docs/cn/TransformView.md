# `<TransformView />` 可变视图
TransformView 组件定义一个可变视图, 支持双指按捏缩放、单指触摸移动手势, 使用纯 JS 实现, 同时支持 Android 和 iOS。

## Props
| Prop | Type | Default | Note |
|---|---|---|---|
| [View props...](https://facebook.github.io/react-native/docs/view.html) |  |  | TransformView 组件继承 View 组件的全部属性。
| containerStyle | View.style |  | 内部容器样式。
| maxScale | number |  | 最大缩放倍数。
| minScale | number |  | 最小缩放倍数。
| magnetic | bool | true | 磁性边框, 当缩放后尺寸小于视图尺寸时自动放大到视图大小。
| tension | bool | true | 拉拽阻力, 当图片边缘在视图内时继续拉拽有阻力效果。

## Events
| Event Name | Returns | Notes |
|---|---|---|
| [View events...](https://facebook.github.io/react-native/docs/view.html) |  | TransformView 组件继承 View 组件的全部事件。
| onWillTransform | translateX, translateY, scale | Transform 开始, 三个参数分别为 x 坐标、y 坐标、缩放倍数。
| onTransforming | translateX, translateY, scale | Transform 进行中, 三个参数分别为 x 坐标、y 坐标、缩放倍数。
| onDidTransform | translateX, translateY, scale | Transform 结束, 三个参数分别为 x 坐标、y 坐标、缩放倍数。
| onWillMagnetic | translateX, translateY, scale, newX, newY, newScale | 磁性边框效果开始前调用，返回 true 允许磁性边框效果，否则阻止磁性边框效果效果， magnetic = true 时有效。
| onDidMagnetic | translateX, translateY, scale | 磁性边框效果结束时调用, 三个参数分别为 x 坐标、y 坐标、缩放倍数。
| onPress | event | 单击事件, 触摸结束时调用, 与 TouchableOpacity.onPress 一致。
| onLongPress | event | 长按事件, 按压组件超过 500ms 时调用, 与 TouchableOpacity.onLongPress 一致。

<!--
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
<TransformView
  style={{backgroundColor: '#fff', flex: 1, alignItems: 'center', justifyContent: 'center'}}
  minScale={0.5}
  maxScale={2}
>
  <Image style={{width: 375, height: 300}} resizeMode='cover' source={require('../images/teaset1.jpg')} />
</TransformView>
```


## Screenshots
![](https://github.com/rilyu/teaset/blob/master/screenshots/14-TransformView.png?raw=true)



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