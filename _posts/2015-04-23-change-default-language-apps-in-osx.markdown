---
layout: post
title:  "Change Default Language Apps in OSX"
date:   2015-04-23 00:11:50
categories: [osx, default language, AppleLanguages]
---

By default, Some Applications will select the first available translation from the list in your language list (depending on what version of OSX you're using).

If you want to use a different translation from the one that is automatically selected, you can run the following in Terminal.app:

{% highlight bash %}
defaults write -app AppName AppleLanguages '(de, en)'
{% endhighlight %}

(Use whatever language codes you want, replacing Deutsch and English. It won't work if there isn't a translation file for the language you want.) Some versions of OS X don't accept -app AppName and emit Can't determine domain name for application AppName. In that case use namespace of app in place of -app AppName.

If you want to unset it (that is, return to using the system settings), run this:

{% highlight bash %}
defaults delete -app Gnucash AppleLanguages
{% endhighlight %}

If you have questions, suggestions or any feedback can write in the blog comments or [email me](http://garamburu.com/contact/)