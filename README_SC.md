#  PDF Bookmarks Adder

本工具用于Markdown格式的书签文件，并将这些书签添加到指定的PDF文档中。

## 系统要求

在使用本工具前，请确保您的系统中已安装以下必要的Python库：

- `fitz` (亦称PyMuPDF)：一个用于PDF处理的高效能库。

您可以使用pip命令行工具安装未安装的库：

```bash
pip install PyMuPDF
```

## 使用指南

1. 准备您的书签文件，书签文件需要以OCR或其他方法从源文档中提取，并保存为Markdown（.md）格式。书签应以Markdown的标题格式呈现，每个书签的标题后应紧跟一个`@`符号和对应的页码。请将此文件放置于`input`目录下。
   
   书签文件示例：

   ```markdown
   # 第1章 @10
   ## 第1.1节 @12
   ## 第1.2节 @14
   # 第2章 @20
   ```

2. 将待添加书签的PDF文件放置于`input`目录下。

3. 在`main.ipynb`文件中更新以下路径配置：

   - `bookmarks_md_path`：书签Markdown文件的路径。
   - `pdf_path`：源PDF文件的路径。
   - `output_pdf_path`：带有书签的输出PDF文件的路径。

4. 执行脚本以添加书签到PDF文件内。
