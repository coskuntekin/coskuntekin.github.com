---
title: 'Internet Explorer &#8216;da Debug Yapmak'
author: coskun tekin
layout: post
permalink: /internet-explorer-da-debug-yapmak/
categories:
  - Genel
tags:
  - Debug
  - DevTools
---
Sayfaniz internet explorer (özellikle; ie8, ie9) icin yanlıs yorumlanan kod satırlarına sahip ise debug yapmak kacınılmaz olmaktadir. Internet explorer &#8216;da debug yapmanin en iyi yollarindan biride firebug lite kullanmaktir.
Firebug lite ile online ya da offline (local) calisabilirsiniz.

#### **Stable bookmarklet**

Firebug lite &#8216;i bookmark &#8216;a ekleyerek calisabilirsiniz. Bunun icin [buradaki][1] linki bookmark &#8216; a eklemeniz kafi.

#### **Stable Live Link**

Aşagıdaki kod satırını sayfanin `head` taglari arasina yazmaniz yeterli olacaktir.

{% highlight html %}
<script type="text/javascript" src="https://getfirebug.com/firebug-lite.js"></script>
{% endhighlight %}

#### **Stable local link**

Yine benzer bir yontemle firebug lite [buradan][2] indirdikten sonra asagidaki kodu `head` taglari arasina yazarak firebug lite ile debug yapabilirsiniz.

{% highlight html %}
<script type="text/javascript" src="/local/path/to/firebug-lite-debug.js"></script>
{% endhighlight %}

Daha fazla ayrinti icin [buraya][3] tıklayabilirsiniz.

Eger linux sistem &#8216;de ie browser install etmek istiyorsaniz [buradaki][4] yaziya kisaca goz atabilirsiniz

 [1]: http://javascript:%28function%28F,i,r,e,b,u,g,L,I,T,E%29%7Bif%28F.getElementById%28b%29%29return;E=F%5Bi+%27NS%27%5D&&F.documentElement.namespaceURI;E=E?F%5Bi%20%27NS%27%5D%28E,%27script%27%29:F%5Bi%5D%28%27script%27%29;E%5Br%5D%28%27id%27,b%29;E%5Br%5D%28%27src%27,I%20g%20T%29;E%5Br%5D%28b,u%29;%28F%5Be%5D%28%27head%27%29%5B0%5D%7C%7CF%5Be%5D%28%27body%27%29%5B0%5D%29.appendChild%28E%29;E=new%20Image;E%5Br%5D%28%27src%27,I%20L%29;%7D%29%28document,%27createElement%27,%27setAttribute%27,%27getElementsByTagName%27,%27FirebugLite%27,%274%27,%27firebug-lite.js%27,%27releases/lite/latest/skin/xp/sprite.png%27,%27https://getfirebug.com/%27,%27#startOpened%27%29;
 [2]: https://getfirebug.com/releases/lite/latest/firebug-lite.tar.tgz
 [3]: https://getfirebug.com/firebuglite
 [4]: http://www.coskuntekin.com/linux-sistemde-ie-browser/
