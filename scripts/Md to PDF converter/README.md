---
source-git-commit: a517442244806bc6aef0f5bfb165c5d4f67341be
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 0%

---
# Markdown到PDF转换器

此文件夹包含预处理和转换脚本，用于从此存储库生成文档页的PDF版本。

## 为什么会存在这种情况

文档源文件使用标准markdown工具无法理解的Adobe平台特定的markdown语法（折叠内容块、警告标注和图像属性扩展）。 此脚本规范化该语法，并使用[md-to-pdf](https://github.com/simonhaenisch/md-to-pdf)将文件转换为PDF，同时压缩图像以使输出文件大小可管理。

## 先决条件

- [Node.js](https://nodejs.org/)（v18或更高版本）
- `node_modules/`中已安装依赖项。 如果需要重新安装，请从此文件夹运行`npm ci`。

## 使用情况

从&#x200B;**存储库root**&#x200B;运行脚本，将路径传递给要转换的markdown文件：

```
node "scripts/Md to PDF converter/preprocess-for-pdf.js" <path/to/file.md>
```

**示例：**

```
node "scripts/Md to PDF converter/preprocess-for-pdf.js" help/substance-3d-general/openpbr/openpbr-overview.md
```

PDF写入到与源文件&#x200B;**相同的**&#x200B;目录中。 转换过程中创建的临时文件（`*.pdf-ready.md`和`_pdf-images/`）在成功时自动删除。 如果转换失败，保留它们以帮助调试。

## 脚本的功能

| 源语法 | PDF输出 |
|---|---|
| `+++Title`/`+++`个折叠内容块 | 内容始终可见的`#####`标题 |
| `>[!NOTE]`个警报标注 | 带有粗体&#x200B;**注：**&#x200B;前缀的标准块形引号 |
| `![](path){width="N"}`个图像属性 | 保留指定宽度的`<img>`标记 |
| 标记图像链接到`.pdf`文件 | 已删除（仅Web自下载引用） |
| `hold:`前页键值 | 已删除（仅平台元数据） |
| 所有图像 | 调整到最大1200像素宽，以80%的品质重新编码为JPEG |
| 所有表 | 通过插入的CSS删除边框和背景 |
