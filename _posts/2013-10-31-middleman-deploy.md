---
title: Middleman Deploy
layout: post
tags:
  - Middleman
  - Middleman Deploy
---
Middleman ile build edilen bir projenin yine middleman ile nasıl deploy edilebilecegi sorusunun cevabı.

<!--more-->

#### **Add Gemfile**

`gem "middleman-deploy"` ya da `gem install middleman-deploy`

#### **Activate Middleman Deploy**

Proje, build etmeden once ya da build ettikten sonra deploy edilebiler.

{% highlight ruby %}
activate :deploy do |deploy|
  # ...
  deploy.build_before = true # default: false
end
{% endhighlight %}

#### **Deploy Edilebilen Platformlar**

**rsync**

{% highlight ruby %}
activate :deploy do |deploy|
  deploy.method = :rsync
  deploy.host   = "www.example.com"
  deploy.path   = "/srv/www/site"
  # Optional Settings
  # deploy.user  = "tvaughan" # no default
  # deploy.port  = 5309 # ssh port, default: 22
  # deploy.clean = true # remove orphaned files on remote host, default: false
end
{% endhighlight %}

**GitHub Page**

{% highlight ruby %}
activate :deploy do |deploy|
  deploy.method = :git
  # Optional Settings
  # deploy.remote = "custom-remote" # remote name or git url, default: origin
  # deploy.branch = "custom-branch" # default: gh-pages
end
{% endhighlight %}

**FTP**

{% highlight ruby %}
activate :deploy do |deploy|
  deploy.method   = :ftp
  deploy.host     = "ftp.example.com"
  deploy.path     = "/srv/www/site"
  deploy.user     = "tvaughan"
  deploy.password = "secret"
end
{% endhighlight %}

**SFTP**

{% highlight ruby %}
activate :deploy do |deploy|
  deploy.method   = :sftp
  deploy.host     = "sftp.example.com"
  deploy.path     = "/srv/www/site"
  # Optional Settings
  # deploy.user     = "tvaughan" # no default
  # deploy.password = "secret" # no default
end
{% endhighlight %}

Daha ayrıntılı bilgi için [buraya][2] tıklayabilirsiniz.  
Tek bir method ile birden fazla platforma deploy yapmak istiyorsaniz [suradaki][3] issue'yu inceleyebilirsiniz.

 [1]: http://www.coskuntekin.com/middleman-config-rb
 [2]: https://github.com/tvaughan/middleman-deploy
 [3]: https://github.com/tvaughan/middleman-deploy/pull/44
