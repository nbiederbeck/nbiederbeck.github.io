---
layout: post
---

If you added a new font to your system, you need to rebuild the font cache of matplotlib before you can use it.

{% highlight bash %}
fc-cache  # reload system font cache
rm -fv $HOME/.cache/matplotlib/fontlist*.json
python -c "from matplotlib.font_manager import findfont; findfont('sans', rebuild_if_missing=True)"
{% endhighlight %}
