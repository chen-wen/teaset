# `<SegmentedView />` 分段器
SegmentedView 组件定义一个分段器组件, 一般用于同一页面中多项内容分段显示。<br/>SegmentedView 组件为 [`<SegmentedBar />`](./SegmentedBar) 、 [`<Projector />`](./Projector.md) /  [`<Carousel />`](./Carousel.md) 的易用性封装复合组件。

## Props
| Prop | Type | Default | Note |
|---|---|---|---|
| [View props...](https://facebook.github.io/react-native/docs/view.html) |  |  | SegmentedView 组件继承 View 组件的全部属性。
| type | string | 'projector' | 分段器类型。<br/>- projector: 幻灯机, 内容页面使用[`<Projector />`](./Projector.md)组件渲染<br/>- carousel: 走马灯, 内容页面使用[`<Carousel />`](./Carousel.md)组件渲染
| barPosition | string | 'top' | 分段工具条位置。<br/>- top: 顶部<br/>- bottom: 底部
| barStyle | 同View.style |  | 分段工具条样式。
| justifyItem | string | 'fixed' | 分段工具条Item 排列模式。<br/>- fixed: 固定位置等宽排列<br/>- scrollable: 可滚动，Item 数量较多一屏显示不下时使用这种模式
| indicatorType | string | 'itemWidth' | 分段工具条激活指示器类型。<br/>- none: 无<br/>- boxWidth: 等分区间宽度<br/>- itemWidth: Item 内容宽度
| indicatorPosition | string | 'bottom' | 分段工具条激活指示器位置。<br/>- top: 上方<br/>- bottom: 下方
| indicatorLineColor | string |  | 激活指示器颜色，默认值在 Theme 中设置。
| indicatorLineWidth | number |  | 激活指示器线宽度，默认值在 Theme 中设置。
| indicatorPositionPadding | number |  | 激活指示器与上边界或下边界的距离，默认值在 Theme 中设置。
| animated | bool | true | 分段工具条改变激活 Item 时是否有动画效果。
| autoScroll | bool | true | 分段工具条是否自动滚动激活 Item 到容器中间，仅 justifyItem 为 'scrollable' 时有效。
| activeIndex | number |  | 分段工具条激活 Item 序号。

## Events
| Event Name | Returns | Notes |
|---|---|---|
| [View events...](https://facebook.github.io/react-native/docs/view.html) |  | SegmentedView 组件继承 View 组件的全部事件。
| onChange | index | 改变当前页面时调用, index 为当前 Sheet 序号。

## Static Props
| Prop | Type | Default | Note |
|---|---|---|---|
| [Sheet](#segmentedviewsheet--props) | class |  | 分段器 Sheet 组件。

<!--
## Methods
None.

## Static Methods
None.
-->

## `<SegmentedView.Sheet />` Props
| Prop | Type | Default | Note |
|---|---|---|---|
| [View props...](https://facebook.github.io/react-native/docs/view.html) |  |  | SegmentedView.Sheet 组件继承 View 组件的全部属性。
| title | string<br/>number<br/>element |  | 标题, 可以是字符串、数字或 React Native 组件。
| titleStyle | 同Text.style |  | 标题样式, 当 title 类型为 element 时无效。
| activeTitleStyle | 同Text.style |  | 激活状态标题样式, 当 title 类型为 element 时无效。
| badge | string<br/>number<br/>element |  | 徽章, 可以是字符串、数字或 React Native 组件, 为字符串、数字时使用 `<Badge />`组件渲染。

## Example
简单用法
```
<SegmentedView style={{flex: 1}} type='projector'>
  <SegmentedView.Sheet title='one' badge={1}>
    <View style={{flex: 1, alignItems: 'center', justifyContent: 'center'}}>
      <Label type='detail' size='xl' text='Segment one' />
    </View>
  </SegmentedView.Sheet>
  <SegmentedView.Sheet title='two'>
    <View style={{flex: 1, alignItems: 'center', justifyContent: 'center'}}>
      <Label type='detail' size='xl' text='Segment two' />
    </View>
  </SegmentedView.Sheet>
  <SegmentedView.Sheet title='three'>
    <View style={{flex: 1, alignItems: 'center', justifyContent: 'center'}}>
      <Label type='detail' size='xl' text='Segment three' />
    </View>
  </SegmentedView.Sheet>
</SegmentedView>
```


## Screenshots
![](https://github.com/rilyu/teaset/blob/master/screenshots/12-SegmentedView.png?raw=true)



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