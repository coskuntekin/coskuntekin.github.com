---
title: Variable, Mixin, Function, Silent Class
author: coskun tekin
layout: post
permalink: /variable-mixin-function-silent-class/
categories:
  - Genel
tags:
  - Sass
---
Sass, best practices için hangisi ne amaçla kullanılmalı?

<!--more-->

#### **Variable**

Variable, proje icinde sıklıkla tekrar edebilecegi ongorulen property leri anlamlı hale getirmek icin kullanılabilir.

#### **Mixin**

Birden fazla property i tek bir baslık altında toplamada, ustaca kullanılabilir. Örneğin, Browser prefix lerini her defasında uzun uzun belirtmek yerine akıllıca yazılmıs bir mixin ile tek satırda border-radius, gradient, box-shadow gibi CSS3 property leri hızlı ve pratik bir sekilde kullanılabilir. Sadece browser prefixleri icin degil, uretken class lar icinde kullanılabiilir.

{% highlight sass %}
=graphic-background ($image-name)
  width: image-width($image-name)
  height: image-height($image-name)
  background-image: image_url($image-name)

+graphic-background(my-image)
{% endhighlight %}

{% highlight sass %}
=rounded($radius: 50%)
  -webkit-border-radius: $radius
  -moz-border-radius: $radius
  border-radius: $radius
  
+rounded
{% endhighlight %}

#### **Function**

Function, Sass içersindeki genellikle matematiksel hesaplar icin kullanılabilir.

{% highlight sass %}
@function strip-unit($value)
    @return $value / ($value * 0 + 1)

@for $i from 1 through 7
  .list-btn
    & > li:nth-child(#{$i})
      +animation-delay(400ms + ($i*30))  
{% endhighlight %}

#### **Silent Class**

Sadece Sass da kendini gösteren CSS de hayalet olan class tır. Benzer property lere sahip class ları bir araya getirmede kullanılabilir.(Silent class Sass 3.2 surumuyle birlikte aktif olmustur.)

{% highlight sass %}
%fluid
  float: left
  width: 100%
  height: auto

.header
 @extend %fluid
{% endhighlight %}
