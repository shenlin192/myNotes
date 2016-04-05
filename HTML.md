## 各种小问题
- Attributes provide additional information about HTML elements.
- Meta data means data about data. HTML meta data is data about the HTML document.
- Browsers display \<strong\> as \<b\>, and \<em\> as \<i\>.  

However, there is a difference in the meaning of these tags: \<b\> and \<i\> defines bold and italic text,  
but \<strong\> and \<em\> means that the text is "important".

- Both the width, height, and style attributes are valid in the latest HTML5 standard.  

We suggest you use the style attribute. It prevents styles sheets from changing the original size of images:

##CSS 与 Javascript 的外联（external style sheet）和内联（internal style sheet）
总体而言，外联和内联各有优点，可综合实际情况选择适合的级联方式。

 总结一下：外联优点：css在同一个文件中，当页面需要修改的时候只需要修改一个文件即可，方便维护。

                     缺点：HTTP请求多，浏览器要加载完CSS才能渲染页面，因此影响页面的性能。

               内置优点：内联 CSS 可以有效减少 HTTP 请求，提升页面性能，缓解服务器压力。由于浏览器加载完 CSS 才能渲染页面，因此能防止 CSS 文件无法读取而造成

                             页面裸奔的现象。

                     缺点：每次修改css的时候需要修改多个页面

 

 

Javascrip内联和外置的区别其实也差不多

JavaScript文件外部加载的好处
统一定义JavaScript代码，方便查看，方便维护。
使代码更安全，可以压缩，加密单个JavaScript文件。
浏览器可以缓存JavaScript文件，减少宽带使用（当多个页面同时使用一个JavaScript文件的时候，通常只需下载一次）。
 

JavaScript文件外部加载的注意事项
不要把JavaScript分为多个文件，多个文件会增加服务器的负担，增加服务器的HTTP请求。
一个JavaScript文件也会增大HTTP请求。
 

使用外部JavaScript和CSS   
      很多性能规则都是关于如何处理外部文件的。但是，在你采取这些措施前你可能会问到一个更基本的问题：JavaScript和CSS是应该放在外部文件中呢还是把它们放在页面本身之内呢？   
      在实际应用中使用外部文件可以提高页面速度，因为JavaScript和CSS文件都能在浏览器中产生缓存。内置在HTML文档中的JavaScript 和CSS则会在每次请求中随HTML文档重新下载。这虽然减少了HTTP请求的次数，却增加了HTML文档的大小。从另一方面来说，如果外部文件中的 JavaScript和CSS被浏览器缓存，在没有增加HTTP请求次数的同时可以减少HTML文档的大小。   
      关键问题是，外部JavaScript和CSS文件缓存的频率和请求HTML文档的次数有关。虽然有一定的难度，但是仍然有一些指标可以一测量它。如果一个会话中用户会浏览你网站中的多个页面，并且这些页面中会重复使用相同的脚本和样式表，缓存外部文件就会带来更大的益处。   
      许多网站没有功能建立这些指标。对于这些网站来说，最好的坚决方法就是把JavaScript和CSS作为外部文件引用。比较适合使用内置代码的例外就是网站的主页，如Yahoo!主页和My Yahoo!。主页在一次会话中拥有较少（可能只有一次）的浏览量，你可以发现内置JavaScript和CSS对于终端用户来说会加快响应时 间。   
      对于拥有较大浏览量的首页来说，有一种技术可以平衡内置代码带来的HTTP请求减少与通过使用外部文件进行缓存带来的好处。其中一个就是在首页中内置 JavaScript和CSS，但是在页面下载完成后动态下载外部文件，在子页面中使用到这些文件时，它们已经缓存到浏览器了。  

