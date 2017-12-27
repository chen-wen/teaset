# `ActionSheet{}` 操作选单
ActionSheet 为操作选单静态类, 一般用于触发一个多项子操作供用户选择, 表现形式为从屏幕下方拖出抽屉。<br/>ActionSheet 基于 [Overlay{}](./Overlay.md) 实现。

## Static Methods
| Method | Params | Returns | Notes |
|---|---|---|---|
| [Overlay methods](./Overlay.md) |  |  | ActionSheet 继承 Overlay 的全部静态方法。
| show | items, cancelItem, options | key | 显示一个操作选单, 重写 [Overlay{}](./Overlay.md) 中的同名函数, 输入参数 items 为操作选单项列表, cancelItem(可空)为取消操作项, options(可空)为 ActionSheet.ActionSheetView 其它属性, 参数类型参见 [ActionSheetView](#actionsheetactionsheetview--props)。<br/>返回唯一的浮层 key 值。

## Static Props
| Prop | Type | Default | Note |
|---|---|---|---|
| [ActionSheetView](#actionsheetactionsheetview--props) | class |  | ActionSheet 内容显示组件。

## `<ActionSheet.ActionSheetView />` Props
| Prop | Type | Default | Note |
|---|---|---|---|
| [Overlay.PullView props...](./Overlay.md#overlaypullview--props) |  |  | ActionSheet.ActionSheetView 组件继承 Overlay.PullView 组件的全部属性。
| items | array |  | 操作选单项列表, 数组元素类型为:<br/>type ActionSheetItem {<br/>&ensp;&ensp;title: string,<br/>&ensp;&ensp;onPress: func,<br/>&ensp;&ensp;disabled: bool,<br/>}
| cancelItem | ActionSheetItem |  | 取消操作项。<br/>type ActionSheetItem {<br/>&ensp;&ensp;title: string,<br/>&ensp;&ensp;onPress: func,<br/>&ensp;&ensp;disabled: bool,<br/>}

## `<ActionSheet.ActionSheetView />` Static Props
| Prop | Type | Default | Note |
|---|---|---|---|
| [Item](#actionsheetactionsheetviewitem--props) | class |  | ActionSheet 操作选单项显示组件。

## `<ActionSheet.ActionSheetView.Item />` Props
| Prop | Type | Default | Note |
|---|---|---|---|
| [TouchableOpacity props...](https://facebook.github.io/react-native/docs/touchableopacity.html) |  |  | ActionSheet.ActionSheetView.Item 组件继承 TouchableOpacity 组件的全部属性。
| type | string | 'default' | 类型。<br/>- default: 默认<br/>- cancel: 取消
| title | string<br/>number<br/>element |  | 标题, 可以是字符串、数字或 React Native 组件。
| topSeparator | string<br/>element | 'none' | 上分隔线, 可以是字符串或 React Native 组件。<br/>- none: 无<br/>- full: 满行分隔线<br/>- indent: 缩进分隔线
| bottomSeparator | string<br/>element | 'indent' | 下分隔线, 可以是字符串或 React Native 组件。<br/>- none: 无<br/>- full: 满行分隔线<br/>- indent: 缩进分隔线
| disabled | bool | false | 继承自 TouchableOpacity, 为 true 时组件显示为半透明且不可触摸。

## Example
简单用法
```
let items = [
  {title: 'Say hello', onPress: () => alert('Hello')},
  {title: 'Do nothing'},
  {title: 'Disabled', disabled: true},
];
let cancelItem = {title: 'Cancel'};
ActionSheet.show(items, cancelItem);
```


## Screenshots
![](https://github.com/rilyu/teaset/blob/master/screenshots/17-ActionSheet.png?raw=true)



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
