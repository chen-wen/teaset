# `<Stepper />` 步进器
Stepper 组件定义一个步进器。

## Props
| Prop | Type | Default | Note |
|---|---|---|---|
| [View props...](https://facebook.github.io/react-native/docs/view.html) |  |  | Stepper 组件继承 View 组件的全部属性。
| defaultValue | number | 0 | 初始值, 仅在组件初始化时使用一次, 如不想传入 value 并监听 onChange 保持状态同步,  可使用 defaultValue 代替。
| value | number |  | 当前值。
| step | number | 1 | 步长, 可以是整数或小数。
| max | number |  | 最大值, 默认不限制。
| min | number |  | 最小值, 默认不限制。
| valueStyle | 同Text.style |  | 值显示样式。
| valueFormat | func |  | 格式化值函数, 传入参数为 value, 默认直接使用 value。
| subButton | string<br/>element | '-' | “减“按钮, 可以是字符串或 React Native 组件。
| addButton | string<br/>element | '+' | “加“按钮, 可以是字符串或 React Native 组件。
| showSeparator | bool | true | 是否显示按钮与值之间的分隔线, 如需完全自定义组件样式可设置为 false。
| disabled | bool | false | 是否禁用, 为 true 时组件显示为半透明且不可触摸。
| editable | bool | true | 是否可编辑。

## Events
| Event Name | Returns | Notes |
|---|---|---|
| [View events...](https://facebook.github.io/react-native/docs/view.html) |  | Stepper 组件继承 View 组件的全部事件。
| onChange | value | 当 value 值发生改变时调用。

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
<Stepper />
```

使用 defaultValue、min 和 max, 以下代码设置默认值为1, 最小值为1, 最大值为10
```
<Stepper defaultValue={1} min={1} max={10} />
```

使用 step 和 valueFormat, 以下代码设置步长为0.005(0.5%)并使用一位小数百分比显示值
```
<Stepper
  defaultValue={0.8}
  step={0.005}
  valueFormat={v => (v * 100).toFixed(1) + '%'}
  valueStyle={{minWidth: 60}}
  />
```

自定义
```
<Stepper
  style={{borderWidth: 0}}
  value={this.state.valueCustom}
  valueStyle={{color: '#8a6d3b'}}
  min={0}
  max={100}
  subButton={
    <View style={{backgroundColor: '#fcf8e3', borderColor: '#8a6d3b', borderWidth: 1, borderRadius:4, width: 20, height: 20, alignItems: 'center', justifyContent: 'center'}}>
      <Text style={{color: '#8a6d3b'}}>－</Text>
    </View>
  }
  addButton={
    <View style={{backgroundColor: '#fcf8e3', borderColor: '#8a6d3b', borderWidth: 1, borderRadius:4, width: 20, height: 20, alignItems: 'center', justifyContent: 'center'}}>
      <Text style={{color: '#8a6d3b'}}>＋</Text>
    </View>
  }
  showSeparator={false}
  onChange={v => this.setState({valueCustom: v})}
  />
```


## Screenshots
![](https://github.com/rilyu/teaset/blob/master/screenshots/05a-Stepper.png?raw=true)



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