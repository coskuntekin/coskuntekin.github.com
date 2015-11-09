---
title: Linux Sistemde IE Browser
author: coskun tekin
layout: post
permalink: /linux-sistemde-ie-browser/
categories:
  - Genel
tags:
  - Linux
---
Linux sistemde virtual box ile ie kurulumu aşağıdaki gibi yapılabilir.

#### **Virtual Box Kurulumu**

Kullandiginiz sisteme uygun virtual box surumunu [buradan][1] indirip kurulumunu yapınız.

#### **IE kurulumu**

Curl kurulumunu daha onceden yapmamis iseniz asagidaki komut ile kurubilirsiniz.

{% highlight bash %}
sudo apt-get install curl
sudo apt-get install unar
{% endhighlight %}

Tüm ie versiyonlari (6, 7, 8, 9, 10, 11) icin

{% highlight bash %}
curl -s https://raw.github.com/xdissent/ievms/master/ievms.sh | bash
{% endhighlight %}

Özel bir version icin

{% highlight bash %}
curl -s https://raw.github.com/xdissent/ievms/master/ievms.sh | env IEVMS_VERSIONS="9" bash
{% endhighlight %}

Daha fazla ayrintili bilgi icin [buraya][2] tıklayınız.

 [1]: https://www.virtualbox.org/wiki/Linux_Downloads
 [2]: https://github.com/xdissent/ievms
