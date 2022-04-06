---
layout: post
title:  "Start application on specific workspace in i3"
date:   2021-12-13 18:49:18 +0100
categories: i3 dotfiles
---
First get class name of app by running
{% highlight bash %}
xprop | grep 'WM_CLASS(STRING)'
{% endhighlight %}
and clicking on the window of the app.
Then in .config/i3/config add following line, filling in `<classname>` and `<workspacename>`
{% highlight bash %}
for_window [class=”<classname>“] move container to workspace <workspacename>
{% endhighlight %}
e.g.
{% highlight bash %}
for_window [class=”Spotify”] move container to workspace $ws9
{% endhighlight %}
