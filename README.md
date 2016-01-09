
<!---

This README is automatically generated from the comments in these files:
paper-dialog-behavior.html

Edit those files, and our readme bot will duplicate them over here!
Edit this file, and the bot will squash your changes :)

-->

[![建立状态](https://travis-ci.org/PolymerElements/paper-dialog-behavior.svg?branch=master)](https://travis-ci.org/PolymerElements/paper-dialog-behavior)

_[演示API文档](https://elements.polymer-project.org/elements/paper-dialog-behavior)_


##聚合物对话框


Use `Polymer.PaperDialogBehavior` and `paper-dialog-shared-styles.html` 实施材料设计对话

例如，如果`<paper-dialog-impl>` 实现这一行为：

    <paper-dialog-impl>
        <h2>Header</h2>
        <div>Dialog body</div>
        <div class="buttons">
            <paper-button dialog-dismiss>Cancel</paper-button>
            <paper-button dialog-confirm>Accept</paper-button>
        </div>
    </paper-dialog-impl>

`paper-dialog-shared-styles.html` 为按钮的标题、内容区域和动作区域提供样式。

使用 `<h2>`标签的标题和 `buttons` 类的行动领域。您可以使用
`paper-dialog-scrollable` 元素（在它自己的存储库），如果你需要一个滚动的内容区域。

使用`dialog-dismiss` 和 `dialog-confirm` 属性在交互式控件关闭
对话。如果用户取消与对话 `dialog-confirm`, 这 `closingReason` 将更新
包括 `confirmed: true`.

### 造型

下面的自定义属性和混入可用于造型。

自定义属性 | 描述| 默认
----------------|-------------|----------
`--paper-dialog-background-color` |对话背景颜色                    | `--primary-background-color`
`--paper-dialog-color`            | 对话框前景色                    | `--primary-text-color`
`--paper-dialog`                  | 混入施加到对话               | `{}`
`--paper-dialog-title`            | 混入施加到标题 (`<h2>`) element | `{}`
`--paper-dialog-button-color`     | 按钮区前景色             | `--default-primary-color`

### 无障碍

这个元素 `role="dialog"` 默认。根据不同的方面，它可以是更合适
覆盖此属性与 `role="alertdialog"`.

如果 `modal`被设置时，元件将设置 `aria-modal` 和防止焦点从离开元件。
它还将确保重点仍然在对话框中。

这 `aria-labelledby`属性将被设置到头部元件，如果有的话。


