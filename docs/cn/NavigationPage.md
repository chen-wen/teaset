# `<NavigationPage />` 导航页面
NavigationPage 定义一个导航页面组件, 继承自 [BasePage](./BasePage.md), 在 BasePage 的基础上添加一个 [NavigationBar](./NavigationBar.md) 导航条。

## Props
| Prop | Type | Default | Note |
|---|---|---|---|
| [BasePage props...](./BasePage.md) |  |  | NavigationPage 组件继承 BasePage 组件的全部属性。
| title | string | null | 导航条标题。
| showBackButton | bool | false | 是否显示返回按钮。
| navigationBarInsets | bool | true | 是否为内容区域增加导航条占用空间。<br/>此属性默认为 true, 使得内容不被导航条遮挡, 如果页面内容实用 ScrollView 且需要自行控制 NavigationBar 导航条的显示/隐藏, 那么你需要将此属性设置为 false 并自行在 ScrollView 容器里增加导航条的占用空间, 这样可以在导航条隐藏后把顶部空间利用起来。
| scene | object | Navigator.SceneConfigs.PushFromRight | 继承自 BasePage 并修改默认值。

## Methods
| Method | Params | Returns | Notes |
|---|---|---|---|
| [BasePage methods...](./BasePage.md) |  |  | NavigationPage 组件继承 BasePage 组件的全部方法。
| renderNavigationTitle |  | element | 导航条标题渲染函数, 默认为 this.props.title。
| renderNavigationLeftView |  | element | 导航条左按钮渲染函数, 默认根据 this.props.showBackButton 值决定返回值, 为 true 时返回 NavigationBar.BackButton 组件实例, 否则返回 null。<br/>注: 可以通过 Theme 修改返回按钮的默认标题。
| renderNavigationRightView |  | element | 导航条右侧按钮渲染函数, 默认返回 null。
| renderNavigationBar |  | element | 导航条渲染函数, 一般应重写上面三个函数, 而不是此函数。

## Example
简单用法
```
import React from 'react';
import {View} from 'react-native';

import {NavigationPage, Label} from 'teaset';

class MePage extends NavigationPage {

  static defaultProps = {
    ...NavigationPage.defaultProps,
    title: 'Me',
    showBackButton: false,
  };

  renderPage() {
    return (
      <View style={{flex: 1, alignItems: 'center', justifyContent: 'center'}}>
        <Label type='detail' size='xl' text={this.props.title} />
      </View>
    );
  }

}
```


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