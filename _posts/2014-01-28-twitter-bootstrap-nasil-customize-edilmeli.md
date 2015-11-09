---
title: Twitter Bootstrap Customize Yöntemleri
author: coskun tekin
layout: post
permalink: /twitter-bootstrap-nasil-customize-edilmeli/
categories:
  - Genel
tags:
  - Twitter Bootstrap
---

#### **Custom Class ile Override Etmek**

Sayfada istenmeyen property leri override etmek icin custom class lar kullanılabilir.

{% highlight css %}
panel-custom {
  position: relative;
  margin-top: -30px;
  -webkit-box-shadow: 0 0 3px #dadada;
  box-shadow: 0 0 3px #dadada;
  border: 0;
  z-index: 8;
}
{% endhighlight %}

#### **Variable'lar Kullanarak Customize Etmek**

[Variable][1] &#8216;lar twitter bootstrap&#8217;ı customize etmek icin cok daha akıcı bir kod yazma imkanı sunmaktadır. Ayrıca property ler override edilmeksizin temiz bir css output alınabilir.

Eger [bootstrap-sass][2] &#8216;i kullanıyorsaniz, `_bootstrap-custom.sass` dosyası gem den once import edilmelidir.

{% highlight sass %}
//BOOTSTRAP OVERRIDE
@import partials/bootstrap-custom
//FROM GEM
@import bootstrap
{% endhighlight %}

[1]: http://getbootstrap.com/customize/
[2]: https://github.com/twbs/bootstrap-sass
