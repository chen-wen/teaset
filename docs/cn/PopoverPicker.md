# `PopoverPicker{}` 气泡选择器
PopoverPicker 为气泡选择器静态类, 一般用于触发显示一个数据列表供用户选择, 表现形式为从触发源组件弹出的气泡。<br/>PopoverPicker 基于 [Overlay{}](./Overlay.md) 实现。

## Static Methods
| Method | Params | Returns | Notes |
|---|---|---|---|
| [Overlay methods](./Overlay.md) |  |  | PopoverPicker 继承 Overlay 的全部静态方法。
| show | fromBounds, items, selectedIndex, onSelected, options | key | 显示一个气泡选择器, 重写 [Overlay{}](./Overlay.md) 中的同名函数, 输入参数 fromBounds 为弹出气泡源组件 bounds, items 为可选项列表, selectedIndex 为已选项编号, onSelected 为选择某项时的回调函数, options(可空)为 PopoverPicker.PopoverPickerView 其它属性, 参数类型参见 [PopoverPickerView](#popoverpickerpopoverpickerview--props)。<br/>返回唯一的浮层 key 值。

## Static Props
| Prop | Type | Default | Note |
|---|---|---|---|
| [PopoverPickerView](#popoverpickerpopoverpickerview--props) | class |  | PopoverPicker 内容显示组件。

## `<PopoverPicker.PopoverPickerView />` Props
| Prop | Type | Default | Note |
|---|---|---|---|
| [Overlay.PopoverView props...](./Overlay.md#overlaypopoverview--props) |  |  | PopoverPicker.PopoverPickerView 组件继承 Overlay.PopoverView 组件的全部属性。
| items | array |  | 可选项列表, 数组元素可以是任何类型。
| selectedIndex | number |  | 当前已选择项编号。
| getItemText | func |  | 取 items 数组元素的显示文本, 传入参数为(item, index), item = items[index], 默认直接使用 item
| shadow | bool | true | 是否显示阴影(iOS only)。
| direction | string | 'down' | 继承自 Overlay.PopoverView 并修改默认值。
| align | string | 'center' | 继承自 Overlay.PopoverView 并修改默认值。
| showArrow | bool | true | 继承自 Overlay.PopoverView 并修改默认值。

## `<PopoverPicker.PopoverPickerView />` Events
| Event Name | Returns | Notes |
|---|---|---|
| [Overlay.PopoverView events...](./Overlay.md#overlaypopoverview--props) |  | PopoverPicker.PopoverPickerView 组件继承 Overlay.PopoverView 组件的全部事件。
| onSelected | item, index | 当选择器选择 items 数组某项时调用, item = items[index]。

## `<PopoverPicker.PopoverPickerView />` Static Props
| Prop | Type | Default | Note |
|---|---|---|---|
| [Item](#popoverpickerpopoverpickerviewitem--props) | class |  | PopoverPicker 可选项显示组件。

## `<PopoverPicker.PopoverPickerView.Item />` Props
| Prop | Type | Default | Note |
|---|---|---|---|
| [TouchableOpacity props...](https://facebook.github.io/react-native/docs/touchableopacity.html) |  |  | PopoverPicker.PopoverPickerView.Item 组件继承 TouchableOpacity 组件的全部属性。
| title | string<br/>number<br/>element |  | 标题, 可以是字符串、数字或 React Native 组件。
| selected | bool |  | 是否已选中。

## Example
简单用法, fromView 必须是支持 NativeMethodsMixin 的 React Native 原生组件, 如为复合组件需自行实现 measureInWindow 函数, 可参照[Select.js](/components/Select/Select.js)
```
let items = [
  'Apple',
  'Banana',
  'Cherry',
  'Durian',
  'Filbert',
  'Grape',
  'Hickory',
  'Lemon',
  'Mango',
];
fromView.measureInWindow((x, y, width, height) => {
  PopoverPicker.show(
    {x, y, width, height},
    items,
    this.state.selectedIndex,
    (item, index) => this.setState({selectedIndex: index})
  );
});
```


## Screenshots
![](https://github.com/rilyu/teaset/blob/master/screenshots/20-PopoverPicker.png?raw=true)



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