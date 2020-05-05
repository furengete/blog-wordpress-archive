---
title: "感受 LaTeX"
date: "2016-12-22"
---

$latex \\LaTeX$ - [Wikipedia](https://en.wikipedia.org/wiki/LaTeX) (/ˈlɑːtɛx/ LAH-tekh, also pronounced as /ˈlɑːtɛk/ LAH-tek or /ˈleɪtɛk/ LAY-tek, a shortening of Lamport TeX)，你或许希望先弄明白它的读音。

$latex \\LaTeX$ 起源 引用[大家來學 LaTeX](http://jupiter.math.nctu.edu.tw/~smchang/latex/latex123.pdf), latex123 By Edward G.J. Lee 李果正

1. 先來說一些故事TeX是 Donald E. Knuth 教授的精心傑作，它是個功能非常強大的幕後排版系統，含有彈性很大，而且很低階的排版語言。當初，是因為 Knuth 教授在寫他的大著 TAOCP(The Art of Computer Programming) 時，發覺書商把他書中的數學式子排得太難看了，於是決定自行開發一個非常適合排數學式子的排版語言，這就是 TeX 系統的來由。

不僅僅是談到 TeX 一定會提到 Knuth 教授，只要提到排版，沒有人可以忽略他的 TeX 所帶來的變革、影響，甚至 TeX 已經 20 幾歲了，仍然深深影響著排版界及排版軟體，可見這個排版軟體真的是非同小可。

…

1.2 那麼，LaTeX 又是什麼呢？TeX 是個很低階的排版語言，如果排版時都要從這種低階語言來控制版面的話，那將會非常的煩複，所以，一些經常要用到的功能，都會先去定義好（稱為巨集，macro），這樣排版時才會方便、快速，直接引用已定義好的巨集裡頭的指令就可以了。

原始的 TeX 已經有了一組 macro，是 Knuth 教授所寫的，那就是著名的 Plain TeX，但仍然不夠方便、直觀，於是 Leslie Lamport1.7又寫了另一組的 macro，稱為 LaTeX，主要是把版面配置和文章內容，適度的分開處理，只要使用者選定了一種類別，整本書或整篇文章的結構就是按照這個類別來安排版面，這樣寫文件的人只要專注於文章內容就可以了，版面配置就完全交給 TeX/LaTeX 去處理。

既然 LaTeX 只不過是 TeX 的一大組巨集，那，當然原來的 TeX 的指令，大部份也是可以用在 LaTeX 文稿當中的。而且，LaTeX 並不是目前唯一的 TeX macro，其他如 eplain TeX, ConTeXt, TeXinfo 等都是 TeX macro，也都有他們自成一套的語法。目前的 LaTeX 由 LaTeX 3 Project1.8所維護及發展。

如果談到這裡，你還是霧煞煞的話，類比成 HTML markup 標記語言就能大概知道一些概念了，當然，這和 HTML 標記語言是可相提而無法並論的。如果連 HTML 也不熟悉，那也沒關係啦！這章本來就是在說故事嘛！:-) 只要繼續看後面的內容就行了。

* * *

当你想要完成一篇文章时，可以试着用以下代码编辑你的文本。  
当然，当你看到以下内容时可能依然不明白如何使用，在这里我推荐你先以[ShareLaTeX](https://www.sharelatex.com/)作为首选LaTeX编辑器这不需要在你的电脑中安装任何软件，它是在线的，而且面对个人免费。还有多种模版可供挑选。

你可以先试着打开一个样例项目，看看左边的源码和右边的PDF中的内容是如何对应的，在这之后你就轻松地明白了下面的内容如何使用。

\\documentclass{article} 
%让文档类型是一篇文章
\\usepackage{ctex} 
%TeX原本面向西文写作，这样就可以编译出中文并保留原有风格
\\usepackage{geometry} 
%调用格式设计的一个宏包
\\geometry{a4paper,centering,scale=0.85}
%设置自己喜欢的页面尺寸
\\usepackage{amsmath} 
%当你需要输入数学公式的时候
\\title{标题}
\\author{作者}
\\date{日期}
%以上的导言区域用来设置文档的性质或是自定义一些命令
%接下来开始一个完整的document
\\begin{document} 
%标识出正文的范围（起始处）
\\maketitle 
%实际输出标题
\\tableofcontents 
%这会呈现出与后文对应的目录
\\section{LaTeX} %1 LaTeX
\\subsection{Introduction} %1.1 Introduction
\\subsubsection{Example} %1.1.1 Example
\\section{Mathmode} %2 Mathmode
\\begin{equation}
\\Delta\\vec F(t) = \\frac{d}{dt}\\cdot\\Delta\\vec P(t)
\\end{equation}
%这是一种让数学公式美妙地呈现出来的方式
\\end{document}
%标识出正文的范围（截止处）

%tips
\\setlength{\\parindent}{0pt} %去段首缩进(所有段)
\\noindent %去段首缩进（特定段）
\\newpage %新一页
\\ %另起一行
\\vspace{cm} %空行（厘米)
\\quad %空格

你可以把最上面框框中的内容输入到ShareLaTeX编辑器中然后进行编译（记得在编译之前点击菜单然后把编译器换为XeLaTeX），而且你还可以试着删除或替换一些内容，看看会有什么事情发生，因为这样做会带来一种感觉，希望你能拥有一个好的开始。

* * *

当你想要编辑更加复杂的文章时可能会有更高的需求，在这里我会向你推荐：

1.[Wikibooks](https://en.wikipedia.org/wiki/LaTeX), open books for an open world  
A [PDF](https://upload.wikimedia.org/wikipedia/commons/2/2d/LaTeX.pdf) version is available  
2.[LaTeX cheat sheet](https://wch.github.io/latexsheet/)
