# `<SearchInput />` 搜索输入框
SearchInput 组件定义一个搜索输入框, 与 Input 的区别是有多一个放大镜图标, 在内容为空时且不在编辑状态时居中显示, 否则左对齐。

## Props
| Prop | Type | Default | Note |
|---|---|---|---|
| [TextInput props...](https://facebook.github.io/react-native/docs/textinput.html) |  |  | SearchInput 组件继承 View 组件的全部属性。
| style | 同View.style |  | 组件样式, 也就是组件的容器 View 的样式。
| inputStyle | 同TextInput.style |  | 输入框样式。
| iconSize | number |  | 放大镜图标长宽尺寸, 默认值在 Theme 中设置。
| disabled | bool | false | 是否禁用, 为 true 时组件显示为半透明且不可触摸。
| underlineColorAndroid | string | 'rgba(0, 0, 0, 0)' | 继承自 TextInput 并修改默认值。

## Events
| Event Name | Returns | Notes |
|---|---|---|
| [TextInput events...](https://facebook.github.io/react-native/docs/textinput.html) |  | SearchInput 组件继承 TextInput 组件的全部事件。

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
<SearchInput style={{width: 200}} placeholder='Enter text' />
```

只读
```
<SearchInput style={{width: 200}} placeholder='Enter text' editable={false} />
```

禁用
```
<SearchInput style={{width: 200}} placeholder='Enter text' disabled={true} />
```

自定义
```
<SearchInput
  style={{width: 200, height: 40, backgroundColor: '#fcf8e3', borderColor: '#8a6d3b'}}
  inputStyle={{color: '#8a6d3b', fontSize: 18}}
  iconSize={15}
  value={this.state.valueCustom}
  placeholder='Custom'
  placeholderTextColor='#aaa'
  onChangeText={text => this.setState({valueCustom: text})}
  />
```


## Screenshots
![](https://github.com/rilyu/teaset/blob/master/screenshots/05b-SearchInput.png?raw=true)



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