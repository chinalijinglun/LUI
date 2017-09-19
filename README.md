## sass

```
$class : ljl;  
  
.#{$class}-btn {  
    width : 20px;  
}  
```
## css
variables 变量
mixins 混合
base 基础
colors 颜色
button 按钮
grid 栅格
media 媒体
forms 表单
tables 表格
helpers 帮助

## package.json
run-s 顺序执行 同步
run-p 并行执行 异步

"start": "run-p build watch",异步执行build和watch
"build": "run-s clean sass autoprefixer",同步执行clean、sass和autoprefixer
"clean": "rimraf dist",删除文件夹
"watch": "onchange src -- run-p build",观察src目录，有变动执行run-p build
"autoprefixer": "postcss -u autoprefixer --no-map.inline --autoprefixer.browsers \"last 1 versions\" -r dist/*.css",使用(-u标识符)Autoprefixer替换（-r标识符）`dist/css`目录下的所有`.css`文件，给他们添加厂商前缀代码；https://github.com/postcss/postcss-cli  具体参数
"autoprefixer": "postcss -u autoprefixer --autoprefixer.browsers '&gt; 5%, ie 9' -r dist/css/*"
