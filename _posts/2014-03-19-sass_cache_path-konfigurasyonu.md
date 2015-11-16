---
title: 'Sass Cache Path Konfigurasyonu'
layout: post
tags:
  - Middleman
  - Middleman config.rb
  - Sass
---
Middleman [config.rb][1] de sass_cache klasorunu yeniden set&#8217;lemek icin soyle bir yontem kullanilabilir.

config.rb dosyasinda;

{% highlight ruby %}
# Location of SASS .sass_cache directory.
set :sass_cache_path, File.join('/tmp', "middleman-#{File.basename(Dir.pwd)}", '.cache/sass')
{% endhighlight %}

Degisiklik `http://0.0.0.0:4567/__middleman/config/` de gorulebilir.

Output:
{% highlight ruby %}
:sass_cache_path = "/tmp/middleman-project-title/.cache/sass"
{% endhighlight %}

 [1]: https://gist.github.com/coskuntekin/7335404
