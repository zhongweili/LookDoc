## 前端

### 发展历史

先来看看网页的发展史。

提到前端时，你可能想到的是 HTML、CSS，没错，最早的前端页面就是从 HTML 开始的。超文本标记语言（HyperText Markup Language）简称 HTML，一个 html 文件就是一个静态网页，把这个文件放到 web 服务器上，并在服务器上配置好路由规则，那么当浏览器请求某个 URL 时，web 服务器就会把对应的 html 文件扔给浏览器，再经过渲染，就成了网页。

但是网络上的网页需要有区分，比如面向不同用户要展示不同内容，html 文件不能简单扔给用户，需要有一些逻辑操作。这个任务最初是由 C、C++ 这些语言承担的，服务器操作完后向浏览器扔过去拼接后的字符串，替代了 html 文件，这就是 CGI：Common Gateway Interface。

然而，随着网页内容越来越多，字符串难以完成任务，于是出现了动态 html，也就是在 html 文件中加入了 <%=var%> 这样的变量，这种方案有三种方式可以实现：ASP、JSP、PHP。其中，ASP 对应的是微软的 .NET 技术，JSP 对应的是 java 的方案，PHP 则是开源社区开发的。

但这种动态还不够动态，人们还想动态更新页面内容，更新时只能再请求一次服务器发一份新的 html 文件，这显然不够高效。直到 JavaScript 的出现，完全改变了网站的发展（顺便说一句，JavaScript 与 java 并没有任何关系）。有了 JavaScript，便可以通过修改 html 的 DOM 结构和 CSS 来实现更丰富的网页，不过这些动作都是在浏览器而不是服务器完成的，我猜这时候才慢慢有了前后端的概念吧。

不过很快人们发现，写一大堆 JavaScript 挺麻烦的，使用浏览器的原生 API 操作 DOM 很繁琐，而且经常出错，这时出现了 jQuery，大大简化了代码，终于使得前端开发变得容易。

同时，后端也没闲着，慢慢地发展出高效的模式，借鉴桌面应用程序的 MVC 思想，网站开发也有了经典的 MVC 模式，前后端配合得很默契。之后，网站应用越来越复杂，用户对于交互性的要求越来越高，单纯的 MVC 已经难以胜任，经过改进，MVVM 呼之欲出。

### 技能

前端技术更新很快，每一年都有很多新东西出来，也会有些淘汰的东西，从五花八门的前端框架就能看出来了。前端开发者需要掌握的核心技能包括（最好按顺序学习）：

1. Uniform Resource Locators (aka URLs)
2. Hypertext Transfer Protocol (aka HTTP)
3. Hyper Text Markup Language (aka HTML)
4. Cascading Style Sheets (aka CSS)
5. JavaScript Programming Language (aka ECMAScript 262)
6. JavaScript Object Notation (aka JSON)
7. Document Object Model (aka DOM)
8. Web APIs (aka HTML5 and friends or Browser APIs)

下面列出一些相关的链接

- [HTML 5.2 from W3C](http://w3c.github.io/html/)
- [HTML attribute reference](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes)
- [HTML element reference](https://developer.mozilla.org/en-US/docs/Web/HTML/Element)
- [CSS reference](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference)
- [W3C DOM4](https://www.w3.org/TR/2015/REC-dom-20151119/)
- [ECMAScript® 2017 Language Specification](https://tc39.github.io/ecma262/)
- [Web API Interfaces](https://developer.mozilla.org/en-US/docs/Web/API)
- [HTTP/2](https://http2.github.io/)
- [Introducing JSON](http://json.org/)
- [JSON API](http://jsonapi.org/)

### 框架

几个流行的前端框架

#### 基于 Jquery

入门简单，API 友好，使用广泛，受 MVVM 影响近几年有所没落

#### 基于 Angular

组件多，体验好，风格一致

#### 基于 React

强大，复杂交互都能实现，开发成本低。入门较难，性能不高

#### 基于 Vue

美观，火爆，设计新颖，组件不够多

