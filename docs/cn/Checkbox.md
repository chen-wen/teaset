# `<Checkbox />` 复选框
Checkbox 组件定义一个复选框, 具有选中、非选中两种状态。

## Props
| Prop | Type | Default | Note |
|---|---|---|---|
| [TouchableOpacity props...](https://facebook.github.io/react-native/docs/touchableopacity.html) |  |  | Checkbox 组件继承 TouchableOpacity 组件的全部属性。
| checked | bool | false | 是否勾选。
| defaultChecked | bool | false | 默认是否勾选，仅创建时使用一次，不想自行监听维护 checked 状态时用 defaultChecked 代替。
| size | string | 'md' | 显示尺寸大小。<br/>- lg: 大<br/>- md: 中<br/>- sm: 小<br/>显示效果参见[Screenshots](#screenshots)。
| title | string<br/>number<br/>element |  | 标题, 可以是字符串、数字或 React Native 组件。
| titleStyle | 同Text.style |  | 标题样式, 当 title 类型为 element 时无效。
| checkedIcon | 同Image.source<br/>element |  | 已勾选图标
| checkedIconStyle | 同Image.style |  | 已勾选图标样式
| uncheckedIcon | 同Image.source<br/>element |   | 未勾选图标
| uncheckedIconStyle | 同Image.style |  | 未勾选图标样式
| disabled | bool | false | 继承自 TouchableOpacity, 为 true 时组件显示为半透明且不可触摸。
| hitSlop | 同TouchableOpacity.hitSlop | {top: 8, bottom: 8,<br/>left: 8, right: 8} | 继承自 TouchableOpacity 并修改默认值。

## Events
| Event Name | Returns | Notes |
|---|---|---|
| [TouchableOpacity events...](https://facebook.github.io/react-native/docs/touchableopacity.html) |  | Checkbox 组件继承 TouchableOpacity 组件的全部事件。
| onChange | checked | 当 checked 状态发生变更时调用, 值为修改后的 checked。

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
<Checkbox
  title='Default'
  checked={this.state.checked}
  onChange={checked => shis.setState({checked})}
  />
```

使用 size 属性
```
<Checkbox
  title='Large'
  size='lg'
  checked={this.state.checked}
  onChange={checked => shis.setState({checked})}
  />
```

自定义
```
<Checkbox
  title='Custom'
  titleStyle={{color: '#8a6d3b', paddingLeft: 4}}
  checkedIcon={<Image style={{width: 15, height: 15, tintColor: '#8a6d3b'}} source={require('../icons/checkbox_checked.png')} />}
  uncheckedIcon={<Image style={{width: 15, height: 15, tintColor: '#8a6d3b'}} source={require('../icons/checkbox_unchecked.png')} />}
  checked={this.state.checkedCustom}
  onChange={checked => this.setState({checkedCustom: checked})}
  />
```


## Screenshots
![](https://github.com/rilyu/teaset/blob/master/screenshots/03-Checkbox.png?raw=true)


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