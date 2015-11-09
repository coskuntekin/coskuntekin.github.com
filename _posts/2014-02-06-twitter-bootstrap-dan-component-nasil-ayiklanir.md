---
title: 'Twitter Bootstrap&#8217; dan Component&#8217;ler Nasıl Ayıklanır?'
author: coskun tekin
layout: post
permalink: /twitter-bootstrap-dan-component-nasil-ayiklanir/
categories:
  - Genel
tags:
  - Twitter Bootstrap
---
Twitter Bootstrap ile onepage bir sayfa yazıyorsunuz ve kullanmadıgınız componentleri css dosyasından ayıklamak istiyorsunuz.

<!--more-->

<span class="label label-info">Tips:</span> Oncelikle belirmek gerekir ki bu cozum [bootstrap-sass][1] icin gecerlidir.

Terminal&#8217;e asagida ki kod yazılmalıdır.

<pre>cp $(bundle show bootstrap-sass)/vendor/assets/stylesheets/bootstrap.scss \
</pre>

Sonrasında asagıdaki dosya yolunu projenizin assets file structure &#8216;na gore degistiriniz ve kodu terminal&#8217;de calistiriniz.

<pre>app/assets/stylesheets/bootstrap-custom.scss
</pre>

Artık belirtiginiz dosya yolunda `bootstrap-custom` adında bir dosyanız var. `application.sass` dosyasına import&#8217;ladıgınız `@import 'bootstrap'` dosyasını `@import 'bootstrap-custom'` ile degistiriniz. Akabin de `'bootstrap-custom'` dosyasından kullanmadıgınız componentleri cıkartabilirsiniz.

 [1]: https://github.com/twbs/bootstrap-sass