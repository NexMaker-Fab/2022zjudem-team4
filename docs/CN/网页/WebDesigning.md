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

> A repository is a place where you store ideas, resources, or even share and <br> discuss things with others. Repositories can contain folders and files, images, videos, spreadsheets,<br> and data sets. GitHub lets you add a README file at the same time you create a new repository.<br>
⚫ In the upper-right corner of any page, use the :heavy_plus_sign: drop-down menu, and select New repository.<br>
🔴 Drop-down with option to create a new repository<br>
🔵 In the Repository name box, enter *helloworld1*. <br>
🟢 In the Description box, write a short description.<br>
🟡 Select Add a README file.<br>
🟤 Select whether your repository will be Public or Private.<br>
🟣 Click Create repository.
<br><br><br><br><br><br><br><br><br><br><br>

### Step 2: [Github-Desktop](https://desktop.github.com/)

<br>
<img style="float: right;" width= "500" src="Web/webimg/clone.jpg">

🟤 Click File <br>
🟣 Select clone for to select existing Repository or create new repository <br>
🟡 After selecting clone Select Gihub.com.<br>
🟢 Search or Select directly to your Repository.<br>
🔴 click clone.<br>
🔵 After fetching all Filles then Open your Vs Code.

<br><br><br><br><br><br><br><br><br><br><br>

### Step 3: Vs Code
Visual Studio Code, sometimes known as [VS Code](https://code.visualstudio.com/), is a source-code editor developed by [Microsoft]() using the Electron Framework for [Windows](https://code.visualstudio.com/docs/?dv=win), [Linux](https://code.visualstudio.com/docs/?dv=linux64_deb), and [macOS](https://code.visualstudio.com/docs/?dv=osx).<br> Support for debugging, syntax highlighting, intelligent code completion, snippets, code refactoring, and integrated [Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) are among the features. <br>

## Web Building 
<br>
<img style="float: right;" width= "500" src="Web/webimg/22.jpg">
🟡 Select or open your Repository <br>
🔵 click the Setting <br>
🟢 In the Setting page Select Pages.<br>
🔴 add barnch by selecting Main.<br>
🟣 Select Root or Docs.<br>
🟤 Click Save.

<br><br><br><br><br><br><br><br><br><br><br>

## Markdown 
GitHub Markdown is GitHub's markup language for user content, allowing users of different<br> skill levels to create plain text documents that are displayed in HTML.

### Step 4: Install Nodejs
[Node.js](https://nodejs.org/en/) is a server environment which is open source. Node.js is a cross-platform <br>programming language that works on [Windows](https://nodejs.org/en/download/), [Linux](https://nodejs.org/en/download/), [Unix](https://nodejs.org/en/download/), and [macOS](https://nodejs.org/en/download/).<br> Node.js is a JavaScript runtime environment for the backend. Node.js executes <br> JavaScript code outside of a web browser using the V8 JavaScript Engine.

### Step 5 NPM
 <br>
🟡 Select terminal open new terminal

#### Install docsify & Install Docsify

```
npm i docsify-cli -g
```

🔴 After Installation 
#### Make sure the position and then initialize environment

```
docsify init ./docs 
```
🟢
#### Preview

```
 docsify serve docs
 ```



## QA 

### Sidebar
🔴 Creat File Sidebar.md

```Markdown
<!-- 侧边栏 docs/_sidebar.md -->

+ [Who we are](AboutUs/TeamIntro.md)
   + [OUR VISION](AboutUS/Vision.md)
- **📝 Daily Homework**
   - [1. WEB]()
     - [How to Build web](Web/Web2Designing.md)
   - [2. Arduino basic](https://www.arduino.cc/)
     - [ What is Arduino ](https://www.arduino.cc/en/Guide/Introduction/)
     - [ARDUINO BOARD]()
     - [Arduino Software]()
   - [3. Autodesk]()
     - [CAD](Cad/IntroductionofCad.md)
     - [Fusion](Fusion/Fusion.md)
   - [4. 3D printing]()
- 🛠 Final project
  - topic 
  -🧠 innovation
  - market
  - how to design 
  - how to make
  - SDGs
+ **📝 Contact Us**
-👥 [Contact US](AboutUs/contactUS.md)

```
🔴 open the Index file go to <mark> window.$docsify</mark> then add

```html 
loadSidebar: true,

```

 #### collapsible Sidebar
 to make your sidebar collapsible you just need to these things 
add in <mark> window.$docsify</mark> this code 
```html

 subMaxLevel: 3,
 sidebarDisplayLevel: 1, // set sidebar display level
```
Then insert <mark>script</mark> into document just like the [official plugins's](https://docsify.js.org/#/plugins) usage

```html
<!-- plugins -->
<script src="//cdn.jsdelivr.net/npm/docsify-sidebar-collapse/dist/docsify-sidebar-collapse.min.js"></script>
```

### Navbar

🔴 Creat File Navbar.md
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
🔴 open the Index file go to <mark> window.$docsify</mark> then add
```html
loadNavbar: true,
```

### Search
By default, the hyperlink on the current page is recognized and the content is saved in localStorage.<br> You can also specify the path to the files.

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

### Uploading Image 

### Imoji
Renders a larger collection of emoji shorthand codes. Without this plugin, Docsify is able to render only a limited number of emoji shorthand codes.
add the end of index file
```html
<script src="//cdn.jsdelivr.net/npm/docsify/lib/plugins/emoji.min.js"></script>
```
### Coloumns

### LANGUAGE

normaly your docs file look like this 
```
.
└── docs
    ├── README.md
    ├── index.htm
    ├── Sidebar.md
    └── navbar.md
```
if you want to have more languages you need creat another follder like you want make chinese so you haave have follder like China like this way.

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
then add in the index file 
```html 
homepage: 'home.md',
mergeNavbar: true,
```
### footer

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












## Reference tool

Blogs, wikis, documentation, content management systems

[WorldPress], Wordpress web servier
[Wix]
[Webflow]
[Gitlab]-html,Tech Stack - HTML+CSS+Github
[GitBook]
[VuePress]
[Yuque]
[Mubu]
[Notion]
[wolai]


## Web development

http-server
W3C
HTML
CSS
HTML5
templates  



