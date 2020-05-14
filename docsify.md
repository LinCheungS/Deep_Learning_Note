# docsify
> 一个神奇的文档网站生成工具

## 基本使用
```
# 安装
npm i docsify-cli -g

# 初始化项目
docsify init ./docs

# 本地运行
docsify serve ./docs
```

## 项目结构
- docs
    - **index.html** 入口文件
    - **README.md **默认的渲染
    - **.nojekyll** 用于阻止 GitHub Pages 会忽略掉下划线开头的文件
    - **_sidebar.md** 定制侧边栏
    - 文件夹1
        - 1.md
        - 2.md
    - 文件夹2
        - 1.md
        - 2.md

## Index.html
> 用js为文档添加功能
```
  <script>
  window.$docsify = {
    name: '',
    repo: ''
  }
  </script>

  <script>
    window.$docsify = {
    loadSidebar: true,
    subMaxLevel: 2,
    search: { placeholder: 'Type to search',
              noData: 'No Results!',
              paths: 'auto',
               depth: 6 }}
  </script>

  <script src="//unpkg.com/docsify/lib/docsify.min.js"></script>
  <!-- python 语法高亮 -->
  <script src="//unpkg.com/prismjs/components/prism-bash.js"></script>
  <script src="//unpkg.com/prismjs/components/prism-python.js"></script>
  <!-- 搜索 -->
  <script src="//cdn.jsdelivr.net/npm/docsify/lib/plugins/search.min.js"></script>
  <!-- Latex语法 -->
  <script src="//cdn.jsdelivr.net/npm/docsify-katex@latest/dist/docsify-katex.js"></script>
  <link rel="stylesheet" href="//cdn.jsdelivr.net/npm/katex@latest/dist/katex.min.css"/>
  <!-- 图片放大 -->
  <script src="//cdn.jsdelivr.net/npm/docsify/lib/plugins/zoom-image.min.js"></script>

```
## 插入图片
```

<div align=center>
<img width="350" src="../img/chapter03/3.13_dropout.svg"/>
</div>
<div align=center> 图3.5 隐藏层使用了丢弃法的多层感知机</div>

```
