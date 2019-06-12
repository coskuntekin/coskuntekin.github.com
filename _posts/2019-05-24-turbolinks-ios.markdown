---
layout: post
title:  "Turbolinks IOS"
date:   2019-05-24 20:09:00 +0800
categories: [Rails]
---

Turbolinks IOS Rails camiasinin imdadına yetişen hibrid uygulama yazma imkanı veren bir framework. Ama uygulamanın ne kadarı hibrid ne kadarı native olması gerektiğini sizin karar vermeniz gerekiyor, zira uygulamayı yazmak için biraz da **swift** bilmeniz gerekiyor. 

Ben bu yazıda [turbolinks-ios][turbolinks-ios] reposu üzerinden nasıl örnek bir uygulama yapılabilir onu irdelemek istiyorum. Internette başka örnek uygulamalarda bulabilirsiniz ama bu repo offical olduğu için seed olarak kullanmak daha doğru bir seçim olacaktır. Ama bu o kadarda kolay değil repo biraz eski ve clone'ladıktan sonra üzerinde bazı değişiklikler yapmak gerekiyor.

### Clone & Bundle

Repoyu clone'ladıktan sonra [cocoapods][cocoapods] gem'ini yüklemek gerekiyor. 

{% highlight bash %}
  git clone https://github.com/turbolinks/turbolinks-ios.git
  gem install cocoapods
  # Initialize Cocoapods
  pod init
  # Add this line in Podfile
  use_frameworks!
  pod 'Turbolinks', :git => 'https://github.com/turbolinks/turbolinks-ios.git'
  # Install Dependencies
  pod install
{% endhighlight %}

Swift için yapılması gerekenler şimdilik bu kadar. Lakin uygulama için birde server'a ihtiyacımız var. 

{% highlight bash %}
  # Go to server folder and run bundle
  cd TurbolinksDemo/server
  bundle update
{% endhighlight %}

**demo-server** dosyasını **server** klasörünün içine taşımalıyız. Şimdi de **demo-server**'ı aşağıdaki gibi düzenleyelim. Biz daha önceden **bundle update** yaptığımız için gereksiz kodlardan arındırılmış hali aşağıdaki gibidir.

{% highlight bash %}
  #!/usr/bin/env bash
  set -e
  find-bundle-executable() {
    gem contents bundler | grep "/exe/bundle$" | head -n 1
  }
  warn() {
    echo "$1" >&2
  }
  error() {
    warn "$1"
    exit 1
  }
  warn "Starting the demo server (press ^C to exit)..." >&2
  exec rackup
{% endhighlight %}





[turbolinks-ios]: https://github.com/turbolinks/turbolinks-ios
[cocoapods]: https://cocoapods.org