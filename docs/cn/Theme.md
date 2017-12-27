# `{Theme}` 主题

Theme 是 Teaset 的组件样式定义对象, 用于定义 Teaset 组件的默认样式。

Teaset 提供的大部分组件均支持通过 style 属性定义样式, 可以通过代码修改 Teaset 组件的样式。基于 App 统一风格考虑, 建议通过重定义 Theme 对象的属性来修改 Teaset 组件的样式。

Teaset 提供 default 、 black 、 violet 三种配色方案, 默认值见[ThemeDefault.js](/themes/ThemeDefault.js)、[ThemeBlack.js](/themes/ThemeBlack.js)、[ThemeViolet.js](/themes/ThemeViolet.js), 可以自定义完整的配色方案, 也可使用上述一种方案并修改部分默认值。

建议在代码入口处设置 Theme 定义, 如果在 App 运行过程中修改 Theme 定义, 则需要重新加载已渲染的页面。

## Example
修改配色方案
```
import {Theme} from 'teaset';

Theme.set(Theme.themes.black);

```

修改部分默认值
```
import {Theme} from 'teaset';

Theme.set({
  primaryColor: '#f55e5d',
  backButtonTitle: '返回',
});

```

## Screenshots
![](https://github.com/rilyu/teaset/blob/master/screenshots/00a-Theme2.png?raw=true) ![](https://github.com/rilyu/teaset/blob/master/screenshots/00a-Theme3.png?raw=true)



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