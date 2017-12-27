# `PullPicker{}` 上拉选择器
PullPicker 为上拉选择器静态类, 一般用于触发显示一个数据列表供用户选择, 表现形式为从屏幕下方拖出抽屉。<br/>PullPicker 基于 [Overlay{}](./Overlay.md) 实现。

## Static Methods
| Method | Params | Returns | Notes |
|---|---|---|---|
| [Overlay methods](./Overlay.md) |  |  | PullPicker 继承 Overlay 的全部静态方法。
| show | title, items, selectedIndex, onSelected, options | key | 显示一个上拉选择器, 重写 [Overlay{}](./Overlay.md) 中的同名函数, 输入参数 title 为列表标题, items 为可选项列表, selectedIndex 为已选项编号, onSelected 为选择某项时的回调函数, options(可空)为 PullPicker.PullPickerView 其它属性, 参数类型参见 [PullPickerView](#pullpickerpullpickerview--props)。<br/>返回唯一的浮层 key 值。

## Static Props
| Prop | Type | Default | Note |
|---|---|---|---|
| [PullPickerView](#pullpickerpullpickerview--props) | class |  | PullPicker 内容显示组件。

## `<PullPicker.PullPickerView />` Props
| Prop | Type | Default | Note |
|---|---|---|---|
| [Overlay.PullView props...](./Overlay.md#overlaypullview--props) |  |  | PullPicker.PullPickerView 组件继承 Overlay.PullView 组件的全部属性。
| title | string |  | 列表标题。
| items | array |  | 可选项列表, 数组元素可以是任何类型。
| selectedIndex | number |  | 当前已选择项编号。
| getItemText | func |  | 取 items 数组元素的显示文本, 传入参数为(item, index), item = items[index], 默认直接使用 item

## `<PullPicker.PullPickerView />` Events
| Event Name | Returns | Notes |
|---|---|---|
| [Overlay.PullView events...](./Overlay.md#overlaypullview--props) |  | PullPicker.PullPickerView 组件继承 Overlay.PullView 组件的全部事件。
| onSelected | item, index | 当选择器选择 items 数组某项时调用, item = items[index]。

## `<PullPicker.PullPickerView />` Static Props
| Prop | Type | Default | Note |
|---|---|---|---|
| [Item](#pullpickerpullpickerviewitem--props) | class |  | PullPicker 可选项显示组件。

## `<PullPicker.PullPickerView.Item />` Props
| Prop | Type | Default | Note |
|---|---|---|---|
| [ListRow props...](./ListRow.md) |  |  | PullPicker.PullPickerView.Item 组件继承 ListRow 组件的全部属性。
| selected | bool |  | 是否已选中。

## Example
简单用法
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
PullPicker.show(
  'Select item',
  items,
  this.state.selectedIndex,
  (item, index) => this.setState({selectedIndex: index})
);
```


## Screenshots
![](https://github.com/rilyu/teaset/blob/master/screenshots/19-PullPicker.png?raw=true)



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