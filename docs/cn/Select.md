# `<Select />` 选择框
Select 组件定义一个选择框。

## Props
| Prop | Type | Default | Note |
|---|---|---|---|
| [TouchableOpacity props...](https://facebook.github.io/react-native/docs/touchableopacity.html) |  |  | Select 组件继承 TouchableOpacity 组件的全部属性。
| size | string | 'md' | 显示尺寸大小。<br/>- lg: 大<br/>- md: 中<br/>- sm: 小<br/>显示效果参见[Screenshots](#screenshots)。
| value | any |  | 当前选择的值, 可以是任何类型。
| valueStyle | 同Text.style |  | 值显示样式。
| items | array |  | 可选择列表数组, 数组元素可以是任何类型。
| getItemValue | func |  | 取 items 数组元素的 value 值, 传入参数为(item, index), item = items[index], 默认直接使用 item
| getItemText | func |  | 取 items 数组元素的显示文本或 React Native 组件, 传入参数为(item, index), item = items[index], 默认直接使用 item
| pickerType | string | 'auto' | 选择器类型。<br/>- auto: 自动选择, 当设备为 Pad(宽和高均大于768)时使用 PopoverPicker, 否则使用 PullPicker<br/>- pull: PullPicker<br/>- popover: PopoverPicker
| pickerTitle | string |  | PullPicker 选择器标题。
| editable | bool | true | 是否可编辑。
| icon | string<br/>同Image.source<br/>element | 'default' | 图标, 可以是 string 枚举、 Image.source 或 React Native 组件。<br/>- none: 无图标<br/>- default: 默认图标
| iconTintColor | string |  | 组件右侧指示图标颜色。
| placeholder | string |  | 占位字符串, value 为空时显示此字符串。
| placeholderTextColor | string |  | 占位字符串文本颜色。

## Events
| Event Name | Returns | Notes |
|---|---|---|
| [TouchableOpacity events...](https://facebook.github.io/react-native/docs/touchableopacity.html) |  | Select 组件继承 TouchableOpacity 组件的全部事件。
| onSelected | (item, index) | 当选择器选择 items 数组某项时调用, item = items[index]。

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
this.items = [
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

......

<Select
  style={{width: 200}}
  value={this.state.value}
  items={this.items}
  placeholder='Select item'
  pickerTitle='Default'
  onSelected={(item, index) => this.setState({value: item})}
  />
```

自定义
```
this.customItems = [
  {
    text: 'Long long long long long long long',
    value: 1,
  },
  {
    text: 'Short',
    value: 2,
  }
];

......

<Select
  style={{width: 200, backgroundColor: '#fcf8e3', borderColor: '#8a6d3b'}}
  value={this.state.valueCustom}
  valueStyle={{flex: 1, color: '#8a6d3b', textAlign: 'right'}}
  items={this.customItems}
  getItemValue={(item, index) => item.value}
  getItemText={(item, index) => item.text}
  iconTintColor='#8a6d3b'
  placeholder='Select item'
  pickerTitle='Custom'
  onSelected={(item, index) => this.setState({valueCustom: item.value})}
  />
```


## Screenshots
![](https://github.com/rilyu/teaset/blob/master/screenshots/05-Select1.png?raw=true) ![](https://github.com/rilyu/teaset/blob/master/screenshots/05-Select2.png?raw=true)
![](https://github.com/rilyu/teaset/blob/master/screenshots/05-Select3.png?raw=true)



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