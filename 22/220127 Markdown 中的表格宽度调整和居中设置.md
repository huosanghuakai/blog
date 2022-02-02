# Markdown 中的表格宽度调整和居中设置

Markdown 通过各种方式转换为 html 后表格单元列宽度会无法控制（例如本 blog 使用的 Mytory for Wordpress 方案

查了下资料，发现最实用的是在文本上添加 html 标签，如将 ```列1标题``` 修改为 ```<div  style="width:60px;text-align: center">列1标题</div>```（60px可根据实际页面具体调整）

同样，Markdown 表格本身无法实现单元列标题居中而内容靠左，需要首先通过 Markdown 语法设定单元列靠左，在列标题中设置 ```text-align: center```