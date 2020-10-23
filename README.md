# Source Insight Keymap for Visual Studio Code

该插件在vscode中定义了Source Insight的一些常用快捷键，这样你就可以使用Source Insight中的快捷键在vscode中工作

## 为什么并不是所有的Source Insight快捷键都有效？

由于软件不同，Source Insight和vscode实现的功能不一样，有些在Source Insight中的功能在vscode中并没有对应的功能，还有一个原因就是该插件只是定义了最常用的几个快捷键。

## 怎么参与到该插件的开发？

如果你觉得该插件定义的快捷键不够多，那么你可以参加到该插件的开发中来，这里是该项目在[github上的地址](https://github.com/markwinds/source-insight-keymap)，你可以编辑package.json来添加新的快捷键。当然如果你愿意的话还可以发起一个pull request

## 已经完成的快捷键列表

Action|SI|vscode|vscode command|vscode when
---|---|---|---|---
Go to definition|ctrl+=|F12|editor.action.revealDefinition|editorHasDefinitionProvider && editorTextFocus && !isInEmbeddedEditor
Find previous|F3|shift+F3|editor.action.previousMatchFindAction|editorFocus
Find next|F4|F3|editor.action.nextMatchFindAction|editorFocus
Navigate back|alt+,|alt+left|workbench.action.navigateBack|
Navigate forward|alt+.|alt+right|workbench.action.navigateForward|
Expand selection|ctrl+-|alt+shift+right|editor.action.smartSelect.expand|editorTextFocus
Go to Declaration|ctrl+alt+c|null|editor.action.goToReferences|editorHasReferenceProvider && editorTextFocus && !inReferenceSearchEditor && !isInEmbeddedEditor
Close all file|ctrl+shift+w|ctrl+k ctrl+w|workbench.action.closeAllEditors

## 待完成的功能

- 整合multi-command进插件，实现一个快捷键可以执行多条命令。可用于书签命令的多条实现。