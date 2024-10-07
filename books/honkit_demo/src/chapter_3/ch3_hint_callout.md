# 提示`hint`和插图编号`callout`

## `hint` == `callout` == 提示/警告/错误等特殊格式

演示用插件`callout`（具体是[honkit-plugin-blockquote-callout](https://github.com/intptr-t/honkit-plugin-blockquote-callout))实现的`callout`==`hint`==`alert`，即各种类型的提示/提醒的效果

语法：

```markdown
> [!{type}]
> your text
```

其中`{type}`是下面中的任意一种：

* `NOTE`
* `TIP`
* `IMPORTANT`
* `WARNING`
* `CAUTION`
* `UnsupportedAnnotation`

效果如下的显示：

### 注解=`NOTE`

> [!NOTE]
> **注解**类信息中的`内容`

### 提示=`TIP`

> [!TIP]
> **提示**类信息中的`内容`

### 重要=`IMPORTANT`

> [!IMPORTANT]
> **重要**类信息中的`内容`

### 警告=`WARNING`

> [!WARNING]
> **警告**类信息中的`内容`

### 告诫=`CAUTION`=error=错误

> [!CAUTION]
> **告诫**类信息中的`内容`

### 其他的、普通的block内容=`UnsupportedAnnotation`

> [!UnsupportedAnnotation]
> 
> 没有此处特殊格式的、普通的、block块的内容
> 
> 注意，每行内容之间，要保留一行多余的`>`，才是普通的block内容的格式

## 支持参数自定义

### 举例

* `[!Warning|title:※注]`
  * 把`Warning`的title标题的文字，换成：`※注`

代码：

```markdown
> [!Warning|title:※注]
> 把标题"Warning"换成：`※注`
```

效果：

> [!Warning|title:※注]
> 把标题"Warning"换成：`※注`

## 相关

注意到另外一个（旧的gitbook的）插件：

[fzankl/gitbook-plugin-flexible-alerts: GitBook plugin to convert blockquotes into beautiful and configurable alerts using preconfigured or own styles and alert types.](https://github.com/fzankl/gitbook-plugin-flexible-alerts)

其语法格式和此处很类似

且看到有额外的参数设置：

| Key=关键字 | Allowed value=允许的值 |
| --------- | --------------------- |
| style | One of follwowing values: `callout`, `flat` |
| label | Any text |
| icon | A valid Font Awesome icon, e.g. `fa fa-info-circle` |
| className | A name of a `CSS class` which specifies the look and feel |
| labelVisibility | One of follwowing values: `visible` (default), `hidden` |
| iconVisibility | One of follwowing values: `visible` (default), `hidden` |

但是经过实际测试，此处并不支持这些参数。

记录于此，仅供参考。
