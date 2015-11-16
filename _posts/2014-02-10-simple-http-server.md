---
title: Simple HTTP Server
layout: post
tags:
  - Linux
  - Simple HTTP Server
---
localhost &#8216; da simple HTTP Server kurulumu bir kaç farklı method ile yapılabilir.

#### **Grunt ya da Gulp**

Grunt ya da Gulp ile basit bir HTTP Server kurulumu gerceklestirilebilir.
Ayrıntı icin [buraya][1] tıklayınız.

#### **Python**

Linux base sistemde kurulu olan Python&#8217;nu kullanarak tek bir kod satırı ile HTTP Server kurulumu yapılabilir.

{% highlight bash %}
python -m SimpleHTTPServer
{% endhighlight %}

#### **Prax**

Mac OS X &#8216; de ki [pow][3] &#8216; a alternatif bir cozum olarak kullanılabilir. Ayrıntılı bilgi için [buraya][4] tıklayınız.

 [1]: https://github.com/gruntjs/grunt-contrib-connect
 [2]: https://npmjs.org/package/http-server
 [3]: http://pow.cx/
 [4]: https://github.com/ysbaddaden/prax
