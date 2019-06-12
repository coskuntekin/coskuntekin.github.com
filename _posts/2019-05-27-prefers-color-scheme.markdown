---
layout: post
title:  "Karardı Ekranlar"
date:   2019-05-26 13:36:36 +0800
categories: [CSS]
---

Yıllar önce *Opera* (v12.0 öncesi) internet tarayıcısı ile siteye has özelleştirilmiş stiller yazıp göz yoran *light* renklerin üzerine yazdırıyordum. Ama artık bu işi yapan bir *media query* var.

Çok basit anlamda aşağıdaki gibi kullanılabilir.

{% highlight css %}
  @media (prefers-color-scheme: light) {
    /...
  }
  @media (prefers-color-scheme: dark) {
    /....
  }
{% endhighlight %}

Biraz daha fonksiyonel bir yapı için **:root** içine **var(--color)** şeklinde CSS değişkenlerini kullanarak bir şema oluşturulabilir.

{% highlight css %}
  :root {
    --body-bg: white
    --body-color: black
  }
  @media (prefers-color-scheme: dark) {
    :root {
      --body-bg: black
      --body-color: white
    }
  }
{% endhighlight %}

Artık şemada tanımlanan değişkenleri herhangi bir **Class**'ın içinde **prefers-color-scheme** 'den bağımsız olarak kullanabilirsiniz. Örnek bir yapı için bu sitenin kaynak kodunu inceleyebilirsiniz.

Kaynak: [prefers-color-scheme][prefers-color-scheme]

[prefers-color-scheme]: https://developer.mozilla.org/en-US/docs/Web/CSS/@media/prefers-color-scheme
