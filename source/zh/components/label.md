# Label 组件参考

Label 组件用来显示一段文字，文字可以是系统字体，TrueType 字体或者 BMFont 字体，另外，Label 还具有排版功能。

![label](./label/label.png)

![label-property](./label/label-property.png)

点击**属性检查器**下面的`添加组件`按钮，然后从`添加渲染组件`中选择`Label`，即可添加 Label 组件到节点上。

文字的脚本接口请参考[Label API](../api/classes/Label.html)。

## Label 属性

| 属性 |   功能说明
| -------------- | ----------- |
|String| 文本内容字符串。
|Horizontal Align| 文本的水平对齐方式。可选值有 LEFT，CENTER 和 RIGHT。
|Vertical Align| 文本的垂直对齐方式。可选值有 TOP，CENTER 和 BOTTOM。
|Font Size| 文本字体大小。
|Line Height| 文本的行高。
|Overflow| 文本的排版方式，目前支持 CLAMP，SHRINK 和 RESIZE_HEIGHT。详情见`Label 排版`。
|Enable Wrap Text| 是否开启文本换行。
|File| 指定文本渲染需要的字体文件，如果使用系统字体，则此属性可以为空。
|Use System Font| 布尔值，是否使用系统字体。

## Label 排版

| 属性 |   功能说明
| -------------- | ----------- |
|CLAMP| 文字尺寸不会根据 Bounding Box 的大小进行缩放，Wrap Text 关闭的情况下，按照正常文字排列，超出 Bounding Box 的部分将不会显示。Wrap Text 开启的情况下，会试图将本行超出范围的文字换行到下一行。如果纵向空间也不够时，也会隐藏无法完整显示的文字。
|SHRINK| 文字尺寸会根据 Bounding Box 大小进行自动缩放（不会自动放大，最大显示 Font Size 规定的尺寸），Wrap Text 开启时，当宽度不足时会优先将文字换到下一行，如果换行后还无法完整显示，则会将文字进行自动适配 Bounding Box 的大小。如果 Wrap Text 关闭时，则直接按照当前文字进行排版，如果超出边界则会进行自动缩放。
|RESIZE_HEIGHT| 文本的 Bounding Box 会根据文字排版进行适配，这个状态下用户无法手动修改文本的高度，文本的高度由内部算法自动计算出来。

## 详细说明

Label 组件可以通过往`属性检查器`里的 `File` 属性拖拽 TTF 字体文件和 BMFont 字体文件来修改渲染的字体类型。如果不想继续使用字体文件，可以通过勾选`Use System Font`来重新启用系统字体。

---

继续前往 [Spine 组件参考](spine.md) 说明文档。
