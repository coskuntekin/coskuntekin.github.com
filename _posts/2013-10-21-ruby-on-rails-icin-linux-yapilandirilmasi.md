---
title: Ruby on Rails İçin Linux Yapılandırılması
layout: post
tags:
  - Linux
  - Ruby on Rails
---
Ruby&#8217;inin en stable calistigi ortam Linux olarak gosterilebilir. Bu bağlamda, Ruby on Rails çalışma ortamı için Linux&#8217; ta izlenmesi gereken adımlar aşağıdaki gibi sıralanabilir.

<!--more-->  

#### **Sistemin Kuruluma Hazirlanmasi**

Sistemi guncelemek icin

{% highlight bash %}
sudo apt-get update
sudo apt-get upgrade
sudo apt-get dist-upgrade
sudo reboot
{% endhighlight %}

#### **ZSH, Git ve oh-my-zsh Kurulumu**

zsh kurulumu için;

{% highlight bash %}
sudo apt-get install zsh
{% endhighlight %}

curl kurulumu için;

{% highlight bash %}
sudo apt-get install curl
{% endhighlight %}

git kurulumu icin;

{% highlight bash %}
sudo apt-get install git-core
{% endhighlight %}

git konfigurasyonu icin

{% highlight bash %}
git config --global user.name "Your Name"
git config --global user.email your-email@address.com
{% endhighlight %}

oh-my-zsh kurulumu için;

{% highlight bash %}
curl -L https://github.com/robbyrussell/oh-my-zsh/raw/master/tools/install.sh | sh
chsh -s /bin/zsh
{% endhighlight %}

oh-my-zsh ile ilgili daha fazla bilgiyi [buradan][1] edinebilirsiniz.

#### **RVM ve Ruby Kurulumu**

Ruby Version Management icin ben RVM yukledim. Secim yapmak icin [buraya][2] tıklayabilirsiniz.

{% highlight bash %}
\curl -L https://get.rvm.io | bash -s stable --ruby
{% endhighlight %}

Yukleme tamamlandıktan sonra;

{% highlight bash %}
rvm get stable --autolibs=enable
rvm install ruby
rvm --default use ruby-2.1.1
{% endhighlight %}

#### **Node.js Kurulumu**

{% highlight bash %}
sudo apt-get install nodejs
{% endhighlight %}

#### **Gem Manager Version Kontrolu**

{% highlight bash %}
gem -v
{% endhighlight %}

Version&#8217;un guncel olup olmadıgını [buradan][3] kontrol edebilirsiniz. Eger guncel degilse;

{% highlight bash %}
gem update --system
{% endhighlight %}

#### **RVM Gemsets Seçimi ve Gem Update**

{% highlight bash %}
rvm gemset list
{% endhighlight %}

output:

{% highlight bash %}
gemsets for ruby-2.1.1
 => (default)
    global
{% endhighlight %}

secim yapmak için;

{% highlight bash %}
rvm gemset use global
{% endhighlight %}

yeni bir gemset olusturmak icin

{% highlight bash %}
rvm gemset create workflow
{% endhighlight %}

default gemset&#8217;i secmek icin

{% highlight bash %}
rvm --default use ruby-2.1.1@workflow
{% endhighlight %}

Outupdate listesini gormek için;

{% highlight bash %}
gem outdated
{% endhighlight %}

Gem leri guncellemek için;

{% highlight bash %}
gem update
{% endhighlight %}

Gem lerin document dosyalarının yukleme listesinden cıkartmak için;

{% highlight bash %}
echo "gem: --no-document" >> ~/.gemrc
{% endhighlight %}

#### **Rails Kurulumu**

Stable Release version için;

{% highlight bash %}
gem install rails
rails -v
{% endhighlight %}

#### **Rails Application Olusturma**

{% highlight bash %}
rails new .
{% endhighlight %}

Smoke Test için;

{% highlight bash %}
rake -T
{% endhighlight %}

Rails server için;

{% highlight bash %}
rails server
{% endhighlight %}

 [1]: https://github.com/robbyrussell/oh-my-zsh
 [2]: https://www.ruby-toolbox.com/categories/ruby_version_management
 [3]: https://rubygems.org/gems/rubygems-update
 [5]: http://railsapps.github.io/rails-composer/
