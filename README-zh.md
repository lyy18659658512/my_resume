# 功能

* 简单易用，支持单页或多页，A4尺寸的简历生成器。
* 适合打印，直接用浏览器打印或另存为 PDF。
* 用 yaml 编写简历。所有内容都存储在数据文件中。
* 通过编辑 `config.yaml` 添加/删除板块、调整板块顺序。
* 板块名称可在 `config.yaml` 中自定义，因此你可以用任何语言编写。

[这里有一篇关于本项目的博客](https://mertbakir.gitlab.io/projects/resume-a4/)。

# 使用方法

## 下载

1. 创建一个 hugo 项目。
2. 进入 themes 文件夹。
3. 克隆本主题。

```
cd themes
git clone https://gitlab.com/mertbakir/resume-a4.git
```

或作为子模块添加

```
git submodule add https://gitlab.com/mertbakir/resume-a4.git themes/resume-a4
```

## 启动

1. 从 `exampleSite` 目录下复制 `config.yaml` 到 hugo 项目的根目录。
2. 打开 `config.yaml`，填写你的相关信息。
3. 从 `exampleSite` 目录下复制 `data` 文件夹到 hugo 项目的根目录。你只需要这个文件夹。
4. 用 yaml 文件创建你的简历。

## 配置文件

* 你可以添加/删除板块。
* 可以添加任意多页。（不过，别忘了简历的目标，简明扼要更好。招聘官一般不会一直往下翻。）
* 配置文件中“features”的顺序很重要。

### 自定义 CSS

如果你想做简单的样式修改，可以复制 `exampleSite` 目录下的 ```\assets``` 文件夹。

### 头像

在 `config.yaml` 中设置头像链接，图片可以放在 `static` 文件夹下。如果不想添加照片，可以将其设为 ```false```。

### 发表作品

你可以在配置文件中更改 `publications` 板块的 `style`。支持 APA 和 IEEE 两种标准。如果标准有误，欢迎在 gitlab 上反馈或提交合并请求。我不是引用标准方面的专家。

## 打印 | 另存为 PDF

在 ```exampleSite\assets\custom.scss``` 文件中有一个用于打印 href 属性的代码片段。默认未包含，因为“另存为 PDF”更常用。如果你不喜欢 Firefox 下“另存为 PDF”的效果，可以试试 Chrome 或基于 Chromium 的浏览器。可能是因为 Firefox 不支持 [这个](https://developer.mozilla.org/en-US/docs/Web/CSS/%40page/size)。

# 许可证

本项目开源，遵循 MIT 许可证。若能署名，我会很高兴。<3

> _欢迎建议和贡献。_

# 我的工作流程

1. 做出更改。
2. 删除主项目中的 `resources` 文件夹。
2. 使用该主题构建 hugo 站点：`hugo server`
3. 将主项目中的 `resources` 文件夹复制到主题文件夹 `themes\resume-A4\resources`
4. `git commit` 和 `git push`。
