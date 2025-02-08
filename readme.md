<h1 align="center">前端文档的历史比对</h1>

<div align="center">

![GitHub watchers](https://img.shields.io/github/watchers/dingshaohua-com/diff-html?style=social) ![GitHub stars](https://img.shields.io/github/stars/dingshaohua-com/diff-html?style=social) ![GitHub forks](https://img.shields.io/github/forks/dingshaohua-com/diff-html?style=social)
<br />
![node](https://img.shields.io/node/v/koa?style=flat-square)
<br />
![GitHub repo size](https://img.shields.io/github/repo-size/dingshaohua-com/diff-html?style=flat-square) 
![GitHub package.json version](https://img.shields.io/github/package-json/v/dingshaohua-com/diff-html?style=flat-square) 
![GitHub](https://img.shields.io/github/license/dingshaohua-com/diff-html?style=flat-square) 
![GitHub open issues](https://img.shields.io/github/issues/dingshaohua-com/diff-html?style=flat-square) 
![GitHub closed issues](https://img.shields.io/github/issues-closed/dingshaohua-com/diff-html) 
![GitHub last commit](https://img.shields.io/github/last-commit/dingshaohua-com/diff-html?style=flat-square) 
![GitHub top language](https://img.shields.io/github/languages/top/dingshaohua-com/diff-html?style=flat-square)

</div>
   
需求源自于：富文本编辑器生成文档，并不是单纯的文字组成，其中包括了大量的html标签；但是用户能看到的内容只是可视的文本，所以要求我们在做比对的时候能合理的处理html标签；

这个HTML Diff的主要算法来自于： [csharp-html-diff-algorithm](http://www.rohland.co.za/index.php/2009/10/31/csharp-html-diff-algorithm/)，有C# 和 Ruby版本的实现，但是对汉字分字都有问题；这次在做JS版本的时候，将原有的拆分解析逻辑简单的通过正则来实现；效率上并没有什么影响，相对还要简单很多；暂时还未遇到明显的Bug；

代码的实现上在针对高级浏览器时做了简单web Worker支持，是否以webWorker的方式来使用本程序，还需要由业务开发者来自行判断；

整个代码的执行效率相对较低，再对大文本的比对时，耗时相对较长；比对的时间消耗，主要与文档内的文字数量、差异数量相关；

代码内还有密集运算未进行优化，因为初期只针对高版本的Chrome浏览器，所以优化先放放再说~

源自于[参考一个古老的教程！](https://blog.csdn.net/zjq861124/article/details/8019051)
