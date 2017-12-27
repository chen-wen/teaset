# `Drawer{}` 抽屉
Drawer 为抽屉静态类, 内部视图为 Overlay.PullView 的易用性简单封装。<br/>Drawer 基于 [Overlay{}](./Overlay.md) 实现。

## Static Methods
| Method | Params | Returns | Notes |
|---|---|---|---|
| [Overlay methods](./Overlay.md) |  |  | Drawer 继承 Overlay 的全部静态方法。
| open | view, side, rootTransform options | object | 打开一个抽屉。 参数说明：<br/>- view: 抽屉内部视图内容<br/>- side: 抽屉拉出边, 默认为 'left'<br/>- rootTransform: 根组件转换动画, 默认为 'none'<br/>- options: Drawer.DrawerView 其它属性, 参数类型参见 [DrawerView](#drawerdrawerview--props)<br/>返回值为一个对象, 对象属性说明：<br>- key: 浮层唯一键值<br/>- close: 关上抽屉函数, 调用该函数将关上抽屉

## Static Props
| Prop | Type | Default | Note |
|---|---|---|---|
| [DrawerView](#drawerdrawerview--props) | class |  | Drawer 内容显示组件。

## `<Drawer.DrawerView />` Props
| Prop | Type | Default | Note |
|---|---|---|---|
| [Overlay.PullView props...](./Overlay.md#overlaypullview--props) |  |  | Drawer.DrawerView 组件继承 Overlay.PullView 组件的全部属性。

## `<Drawer.DrawerView />` Events
| Event Name | Returns | Notes |
|---|---|---|
| [Overlay.PullView events...](./Overlay.md#overlaypullview--props) |  | Drawer.DrawerView 组件继承 Overlay.PullView 组件的全部事件。

## Example
简单用法
```
let view = (
  <View style={{backgroundColor: Theme.defaultColor, height: 260}}>
    <View style={{flex: 1, alignItems: 'center', justifyContent: 'center'}}>
      <Label type='detail' size='xl' text='Drawer' />
    </View>
  </View>
);
let drawer = Drawer.open(view, 'bottom');

...

drawer.close(); //如需要可代码手动关上抽屉
```

## Screenshots
![](https://github.com/rilyu/teaset/blob/master/screenshots/20b-Drawer1.png?raw=true) ![](https://github.com/rilyu/teaset/blob/master/screenshots/20b-Drawer2.png?raw=true)


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