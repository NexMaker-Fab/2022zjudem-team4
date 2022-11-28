<h1 style="text-align:center; font-size:2vw" >网页构建</h1>

网页构建有很多方法，例如以下：

1. [Gitlab-html](https://pages.gitlab.io/plain-html/):gitlab 用于构建稳定恒久的网页
2. [VuePress](): 相似于 gitbook
3. [Wordpress]() 使用 WordPress 网页服务器构建网页
4. [Tech Stack]()-- [HTML]()+[CSS]()+[Github]()
5. [Wix]()


## 工具准备和环境配置

### 第一步: Github 
[GitHub](https://github.com/) 是一个能够让主机有权控制和合作的平台。<br> 方便主机不分地区国界与他人合作。<br> 
在这网页指南里会学到 Github 的基础，例如网页部署（repository)，网页分支 (branches)，网页提交 (commit)和提交代码申请 (PR - Pull Request)。<br> 
建立属于自己的 Hello World 网页部署，以及使用 Github PR 功能, <br> 就会获得网页链接，这是一个比较通俗的做法。

在这快速入门指南，会学到：

1. 建立和使用网页部署
2. 管理和经营网页分支
3. 文件改动和网页提交
4. 合并代码

需要个人Github 账号 [GitHub account](https://github.com/) 以及稳定的网络连接。不需要知道怎么打码，使用 command line，或者下载 [Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git).

### A. 建立网页部署
<br>
<img style="float: right;" width= "500" src="Web/webimg/11.jpg">

> 网页部署充当与仓库，可以储存想法和资源，还可以与他人分享讨论。<br> 网页部署内含文件档，文件，照片，视频，电子表格及数据。<br> 每当建立网页部署，Github 都会备有 README 空白网页。<br>
⚫ 在每页网页的右上角，点击 :heavy_plus_sign: , 然后选择建立部署。<br>
🔴 点击建立网页部署。<br> 
🔵 在部署名称框里，输入 *helloworld1*。 <br> 
🟢 在描述框里，输入简短的介绍。<br> 
🟡 点击增加 README file。<br> 
🟤 选择网页部署是否公开，或私人。<br> 
🟣 点击建立。 
<br><br><br><br><br><br><br><br><br><br><br>
 
### 第二步: [Github-桌面](https://desktop.github.com/)

<br>
<img style="float: right;" width= "500" src="Web/webimg/clone.jpg">

🟤 选择文件并点击。 <br> 
🟣 选择克隆现存网页部署或建立新部署。 <br> 
🟡 点击克隆后，点击 Github.com。<br> 
🟢 搜索或点击网页部署。<br> 
🔴 选择克隆。<br> 
🔵 文件更新后，打开 VS Code。 

<br><br><br><br><br><br><br><br><br><br><br>

### 第三步: VS Code
Visual Studio Code, 也称为 [VS Code](https://code.visualstudio.com/), 是一个由 [Microsoft] 开发的代码编辑软件，可用于 Electron Framework for [Windows](https://code.visualstudio.com/docs/?dv=win), [Linux](https://code.visualstudio.com/docs/?dv=linux64_deb), and [macOS](https://code.visualstudio.com/docs/?dv=osx).<br> 适用于支援调试，语法提示，智能代码补全，片段调试，重构代码及合并 [Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)。<br>

## 建构网页 
<br>
<img style="float: right;" width= "500" src="Web/webimg/22.jpg">
🟡 选择或打开网页部署。 <br> 
🔵 点击设置。 <br> 
🟢 选择页面.<br> 
🔴 选择主页，然后增加网页分支。<br> 
🟣 选择 Root 或者 Docs。<br>  
🟤 点击保存。

<br><br><br><br><br><br><br><br><br><br><br>

## Markdown 
GitHub Markdown 是 GitHub's 用户个人内容的语言标记, 方便不同级别的用户建立 HTML 呈现的空白网页。<br> 

### 第四步: 下载 Nodejs
[Node.js](https://nodejs.org/en/) 是一个开源的环境服务器。 Node.js 是一个跨平台的语言编程 <br> 可用于 [Windows](https://nodejs.org/en/download/), [Linux](https://nodejs.org/en/download/), [Unix](https://nodejs.org/en/download/), and [macOS](https://nodejs.org/en/download/).<br> Node.js 也是 JavaScript 运行于后端的环境编程。 <br> Node.js 使用 V8 JavaScript 引擎从网络浏览器以外运转 JavaScript 代码。

### 第五步：NPM
 <br>
🟡 打开终端。 

#### 下载 Docsify

```
npm i docsify-cli -g
```

🔴 完成下载 
#### 确认位置以及环境初始化 

```
docsify init ./docs 
```
🟢
#### 预览

```
 docsify serve docs
 ```



## 问答 

### 侧边栏
🔴 建立 Sidebar.md 

```Markdown
<!-- 侧边栏 docs/_sidebar.md -->

+ [我们的愿景](CN/AboutUS/Vision.md)
- *🛠 **日常作业***
   - [1. 建造网页界面](CN/)
     - [Web](CN/Web/WebDesigning.md)
   - [1. 基本的 Arduino](https://www.arduino.cc/)
     - [ 什么是 Arduino ](https://www.arduino.cc/en/Guide/Introduction/)
     - [ARDUINO BOARD](CN/)
     - [Arduino 软件](CN/)
   - [2. Autodesk](CN/)
     - [CAD](CN/Cad/IntroductionofCad.md)
     - [Fusion](CN/Fusion/Fusion.md)
   - [3. 3D printing]()
-🛠 期末作业
   - 主题
   -🧠 创新
   - 市场
   - 设计方案
   - 设计过程
   - 发展可续性
-👥 [联系我们](AboutUs/contactUS.md)
+ **📝 Contact Us**

```
🔴 打开 Index 文件点击 <mark> window.$docsify</mark> 然后输入

```html 
loadSidebar: true,

```

 #### 卷式关闭侧边栏
 若建立卷式关闭侧边栏，至于在 <mark> window.$docsify</mark> 输入这个代码

```html

 subMaxLevel: 3,
 sidebarDisplayLevel: 1, // set sidebar display level
```
填写 <mark>script</mark> 在文件处，如 [official plugins's](https://docsify.js.org/#/plugins) 作用。

```html
<!-- plugins -->
<script src="//cdn.jsdelivr.net/npm/docsify-sidebar-collapse/dist/docsify-sidebar-collapse.min.js"></script>
```

### Navbar

🔴 建立 Navbar.md

```markdown
<!-- 侧边栏 docs/_navbar.md -->

- [Home]()
- [About US]()
  - [AUGY](AboutUs/AUGY.md)
  - [PETER](AboutUs/Peter.md)
  - [Mahir](AboutUs/Mahir.md)
  - [WIN KEE](AboutUs/Winke.md)
  - [Abdirahim](AboutUs/Hirsi.md)
  - [OMAR KHALED](AboutUs/khaled.md)
  - [MOHAMMED QAID](AboutUs/qaid.md)
  - [WAEL MOHAMMED](AboutUs/wael.md)
  - [ANDRY ERIC](AboutUs/AN.md)

- [:us:]()
    - [CN:cn:](CN/)
  - ع:saudi_arabia:
```
🔴 打开 Index 文件点击 <mark> window.$docsify</mark> 然后输入

```html
loadNavbar: true,
```

### 搜索
网页超链接将会被默认，该内容将保存在 localStorage。<br> 但也可导入特定路径。

```html
<script>
  window.$docsify = {
    search: 'auto', // default

    search: [
      '/',            // => /README.md
      '/guide',       // => /guide.md
      '/get-started', // => /get-started.md
      '/zh-cn/',      // => /zh-cn/README.md
    ],

    // complete configuration parameters
    search: {
      maxAge: 86400000, // Expiration time, the default one day
      paths: [], // or 'auto'
      placeholder: 'Type to search',

      // Localization
      placeholder: {
        '/zh-cn/': '搜索',
        '/': 'Type to search',
      },

      noData: 'No Results!',

      // Localization
      noData: {
        '/zh-cn/': '找不到结果',
        '/': 'No Results',
      },

      // Headline depth, 1 - 6
      depth: 2,

      hideOtherSidebarContent: false, // whether or not to hide other sidebar content

      // To avoid search index collision
      // between multiple websites under the same domain
      namespace: 'website-1',

      // Use different indexes for path prefixes (namespaces).
      // NOTE: Only works in 'auto' mode.
      //
      // When initialiazing an index, we look for the first path from the sidebar.
      // If it matches the prefix from the list, we switch to the corresponding index.
      pathNamespaces: ['/zh-cn', '/ru-ru', '/ru-ru/v1'],

      // You can provide a regexp to match prefixes. In this case,
      // the matching substring will be used to identify the index
      pathNamespaces: /^(\/(zh-cn|ru-ru))?(\/(v1|v2))?/,
    },
  };
</script>
<script src="//cdn.jsdelivr.net/npm/docsify/lib/docsify.min.js"></script>
<script src="//cdn.jsdelivr.net/npm/docsify/lib/plugins/search.min.js"></script>

```

### 上传照片 

### 表情符号
由于 Docsify 只能绘制小部分的表情符号代码，这个插件可以作为替代。
输入此代码在 index file 的后端

```html
<script src="//cdn.jsdelivr.net/npm/docsify/lib/plugins/emoji.min.js"></script>
```
### 行列

### 语言

一般 docs file 将会呈现如以下：  
```
.
└── docs
    ├── README.md
    ├── index.htm
    ├── Sidebar.md
    └── navbar.md
```
若想增加更多的语言，需建立一个新的文件档，如以下:

```
.
└── docs
    ├── README.md
    ├── Home.md
    ├── index.htm
    ├── Sidebar.md
    └── navbar.md
    └── China
     ├── Home.md
     ├── README.md
     ├── index.htm
     ├── Sidebar.md
     └── navbar.md
    └── Arabic
     ├── Home.md
     ├── index.htm
     ├── Sidebar.md
     └── navbar.md
└── README.md   
```
然后在 index file 输入

```html 
homepage: 'home.md',
mergeNavbar: true,
```
### 页脚/脚注

``` html
footer: {
      copy: '<span>Acme &copy; 2022</span>',
      auth: 'by Mavericks',
      pre: '<hr/>',
      style: 'text-align: right;',
      class: 'className',
    },
<!-- add to to the end -->
    <script src="//unpkg.com/docsify-footer-enh/dist/docsify-footer-enh.min.js"></script>
```












## 参考工具

博客, 维基百科, 文献, 内容管理系统

[WorldPress], Wordpress 服务器
[Wix]
[Webflow]
[Gitlab]-html,Tech Stack - HTML+CSS+Github
[GitBook]
[VuePress]
[Yuque]
[Mubu]
[Notion]
[wolai]


## 网页开发

http-server
W3C
HTML
CSS
HTML5
templates  



