docsify 4.6 开始支持嵌入任何类型的文件到文档里。你可以将文件当成 `iframe`、`video`、`audio` 或者 `code block`，如果是 Markdown 文件，甚至可以直接插入到当前文档里。

这是一个嵌入 Markdown 文件的例子。

```markdown
[filename](../_media/example.md ':include')
```

`example.md` 文件的内容将会直接显示在这里：

> This is from the `example.md`

你可以查看 [example.md](https://docsify.js.org/_media/example.md) 原始内容对比效果。

通常情况下，这样的语法将会被当作链接处理。但是在 docsify 里，如果你添加一个 `:include` 选项，它就会被当作文件嵌入。

## 嵌入的类型

当前，嵌入的类型是通过文件后缀自动识别的，这是目前支持的类型：

- **iframe** `.html`, `.htm`
- **markdown** `.markdown`, `.md`
- **audio** `.mp3`
- **video** `.mp4`, `.ogg`
- **code** other file extension

当然，你也可以强制设置嵌入类型。例如你想将 Markdown 文件当作一个 `code block` 嵌入。

```markdown
[filename](../_media/example.md ':include :type=code')
```

你将得到

```markdown
> This is from the `example.md`
```

## 标签属性

如果你嵌入文件是一个 `iframe`、`audio` 或者 `video`，你可以给这些标签设置属性。

```markdown
[抖音](https://www.douyin.com/ ':include :type=iframe width=100% height=400px')
```

[douyin](https://www.douyin.com/ ':include :type=iframe width=100% height=400px')