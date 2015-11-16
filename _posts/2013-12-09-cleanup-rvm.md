---
title: Cleanup RVM
layout: post
tags:
  - RVM
  - RVM cleanup
---
RVM temizligi icin asagidaki adimlar uygulanabilir.

#### **RVM &#8216;nin disk uzerindeki hacmini ogrenmek icin;**

{% highlight bash %}
du -hs ~/.rvm
{% endhighlight %}

#### **Clean Up**

{% highlight bash %}
rvm cleanup all
{% endhighlight %}

Bu kodla beraber temizlenen klasorler; archives, repos, src, log, tmp, gemsets, links

#### **Gemset lerden herhangi birini silmek için;**

{% highlight bash %}
rvm cleanup allrvm gemset delete gemset-name
{% endhighlight %}

#### **Gemset teki tum gem leri silmek icin;**

{% highlight bash %}
rvm gemset empty mygems
{% endhighlight %}


#### **Global cache aktif etmek için;**

{% highlight bash %}
rvm gemset globalcache enable
{% endhighlight %}
