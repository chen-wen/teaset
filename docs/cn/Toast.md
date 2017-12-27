# `Toast{}` 轻提示
Toast 为轻提示静态类, 与 Android 的 Toast 作用类似, 使用纯 JS 编写, 在 iOS 与 Android 下有同样的显示效果。<br/>Toast 基于 [Overlay{}](./Overlay.md) 实现。

## Static Methods
| Method | Params | Returns | Notes |
|---|---|---|---|
| [Overlay methods](./Overlay.md) |  |  | Toast 继承 Overlay 的全部静态方法。
| show | options | key | 显示一个轻提示, 重写 [Overlay{}](./Overlay.md) 中的同名函数, 输入参数 options 为 duration 与 [ToastView](#toasttoastview--props) 的属性合集, 返回唯一的浮层 key 值。<br/>**一般不直接调用此函数**
| message | text, duration, position | key | 显示一个纯文本轻提示框。<br/>duration 默认为 'short', position 默认为 'bottom' 。<br/>默认值可通过 Toast.messageDefaultDuration 、 Toast.messageDefaultPosition 修改。
| success | text, duration, position | key | 显示一个成功轻提示框, 提示框中有一个打勾图标。<br/>duration 默认为 'short', position 默认为 'center' 。<br/>默认值可通过 Toast.defaultDuration 、 Toast.defaultPosition 修改。<br/>**下同**
| fail | text, duration, position | key | 显示一个失败轻提示框, 提示框中有一个打叉图标。
| smile | text, duration, position | key | 显示一个笑脸轻提示框, 提示框中有一个笑脸表情图标。
| sad | text, duration, position | key | 显示一个难过轻提示框, 提示框中有一个难过表情图标。
| info | text, duration, position | key | 显示一个信息轻提示框, 提示框中有一个 Info 图标。
| stop | text, duration, position | key | 显示一个停止轻提示框, 提示框中有一个图标。

## Static Props
| Prop | Type | Default | Note |
|---|---|---|---|
| [ToastView](#toasttoastview--props) | class |  | Toast 内容显示组件。
| defaultDuration | string | 'short' | success, fail, smile, sad, info, stop 函数的 duration 参数默认值, 轻提示框显示时长。<br/>- short: 2000 毫秒<br/>- long: 3500毫秒
| defaultPosition | string | 'center' | success, fail, smile, sad, info, stop 函数的 position 参数默认值, 轻提示框显示位置。参见 [Toast.ToastView](#toasttoastview--props)。
| messageDefaultDuration | string | 'short' | message 函数的 duration 参数默认值。
| messageDefaultPosition | string | 'bottom' | message 函数的 position 参数默认值。

## `<Toast.ToastView />` Props
| Prop | Type | Default | Note |
|---|---|---|---|
| [View props...](https://facebook.github.io/react-native/docs/view.html) |  |  | Toast.ToastView 组件继承 View 组件的全部属性。
| text | string<br/>number<br/>element |  | 轻提示文本, 可以是字符串、数字或 React Native 组件。
| icon | string<br/>同Image.source<br/>element |  | 图标, 可以是 string 枚举、 Image.source 或 React Native 组件。<br/>- none: 无图标<br/>- success: 成功, 打勾图标<br/>- fail: 失败, 打叉图标<br/>- smile: 笑脸表情图标<br/>- sad: 难过表情图标<br/>- info: 信息, 圆圈里一个字母 "i"<br/>- stop: 停止, 圆圈里一个感叹号 "!"
| position | string | 'center' | 轻提示框显示位置。<br/>- top: 窗口靠上位置<br/>- bottom: 窗口靠下位置<br/>- center: 窗口中间位置<br/>top 、 bottom 位置可在 Theme 中设置。

## Example
简单用法
```
Toast.message('Toast message');
Toast.success('Toast success');
Toast.fail('Toast fail');
Toast.smile('Toast smile');
Toast.sad('Toast sad');
Toast.info('Toast info');
Toast.stop('Toast stop');
```

自定义
```
static customKey = null;

showCustom() {
  if (ToastExample.customKey) return;
  ToastExample.customKey = Toast.show({
    text: 'Toast custom',
    icon: <ActivityIndicator size='large' color={Theme.toastIconTintColor} />,
    position: 'top',
    duration: 1000000,
  });
}

hideCustom() {
  if (!ToastExample.customKey) return;
  Toast.hide(ToastExample.customKey);
  ToastExample.customKey = null;
}
```


## Screenshots
![](https://github.com/rilyu/teaset/blob/master/screenshots/16-Toast1.png?raw=true) ![](https://github.com/rilyu/teaset/blob/master/screenshots/16-Toast2.png?raw=true)
![](https://github.com/rilyu/teaset/blob/master/screenshots/16-Toast3.png?raw=true)




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