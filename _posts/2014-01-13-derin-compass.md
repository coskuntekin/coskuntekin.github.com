---
title: 'Derin Compass'
author: coskun tekin
layout: post
permalink: /derin-compass/
categories:
  - Genel
tags:
  - Compass
---
Compass &#8216;ın kendi gölgesinde kalmıs özellikleri.

<!--more-->

#### **Image Dimension**

Image dosyasının width ve height degerlerini compass a okutmak mumkun.

Örneğin;

{% highlight sass %}
.graphic-div
  width: image-width (image.png)
  height: image-height (image.png)
  background-image: image_url (image.png)
{% endhighlight %}

Ayrıntılı bilgi için [buraya][1] tıklayınız.

#### **Experimental**

İstenmeyen browser prefix lerini css de gizlemek icin kullanılabilir.

{% highlight sass %}
=box-sizing($box-size)
  $box-size: unquote($box-size)
  @include experimental(box-sizing, $box-size, -moz, -webkit, not -o, not -ms)
{% endhighlight %}

css output:

{% highlight css %}
.box-div {
    -webkit-box-sizing: border-box;
       -moz-box-sizing: border-box;
            box-sizing: border-box;
}
{% endhighlight %}

Ayrıntılı bilgi için [buraya][2] tıklayınız.

#### **Sprite Dimensions**

Sprite image set olusturmak icin kullanılır.

{% highlight sass %}
$icons: sprite-map('icons/*.png')
i
  +inline-block
  background: $icons

@each $icon in sprite_names($icons)
  .icn-#{$icon}
    +sprite-dimensions($icons, $icon)
    background-position: sprite-position($icons, $icon)
    background-size: image-width(sprite-path($icons)) auto
{% endhighlight %}

Ayrıntılı bilgi için [buraya][3] tıklayınız.

 [1]: http://compass-style.org/reference/compass/helpers/image-dimensions/
 [2]: http://compass-style.org/reference/compass/css3/shared/
 [3]: http://compass-style.org/reference/compass/utilities/sprites/base/
