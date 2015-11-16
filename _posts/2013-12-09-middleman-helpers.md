---
title: Middleman Helpers
layout: post
tags:
  - Middleman
  - Middleman Helpers
---

#### **link_to**

{% highlight haml %}
= link_to 'Link', '/link.html'
= link_to 'Link', '/link'

=link_to 'http://www.homepage.com' do
  %i.fa.fa-home
{% endhighlight %}

#### **image_tag**

{% highlight haml %}
=image_tag 'image.png', class:'image-class'
{% endhighlight %}

#### **Assets Helpers**

{% highlight haml %}
=stylesheet_link_tag 'application'
=javascript_include_tag 'application.js'
=favicon_tag 'favicon.png'
{% endhighlight %}

#### **times**

{% highlight haml %}
-5.times do
{% endhighlight %}
