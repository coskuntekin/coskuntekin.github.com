---
title: 'Middleman &#8211; Hand-crafted frontend development'
author: coskun tekin
layout: post
permalink: /middleman-hand-crafted/
categories:
  - Genel
tags:
  - Middleman
  - Middleman Install
---
HTML sayfalar arasında kaybolmadan kod yazmak için [Middleman][1] kullanılabilir.

#### **Middleman Install ve İlk Ekran**

{% highlight bash %}
gem install middleman
{% endhighlight %}

#### **Init Project**

Middleman de yeni bir proje olusturmak için;

{% highlight bash %}
middleman init my_new_project
{% endhighlight %}

#### **Project Template**

{% highlight bash %}
middleman init my_new_mobile_project --template=html5
{% endhighlight %}

Bir kaç project template; [Middleman-HTML5BP-HAML][2], [middleman-twitter-bootstrap][3]

#### **Middleman Server**

{% highlight bash %}
middleman
{% endhighlight %}

#### **Middleman Build**

{% highlight bash %}
middleman build
{% endhighlight %}

#### **config.rb**

config.rb dosyası ile Middleman&#8217;i customize edebilirsiniz. Ornek bir config.rb için [buraya][4] tıklayınız.

 [1]: http://middlemanapp.com/
 [2]: https://github.com/dannyprose/Middleman-HTML5BP-HAML
 [3]: https://github.com/novemberkilo/middleman-twitter-bootstrap
 [4]: https://gist.github.com/coskuntekin/7335404
