---
layout: docs
title: Character counter
description: Assistive elements for text fields.
group: plugins
counter: true
---

Character or word counters should be used if there is a character or word limit. They display the ratio of characters used and the total character limit.

<div class="list-group my-2 my-lg-5">
    <a href="https://material.io/components/text-fields#anatomy" target="_blank" class="list-group-item list-group-item-action d-flex font-weight-bold">
      <span class="list-group-item-icon lgi-icon-md"></span>
      Material Design guidelines: Text-fields - Assistive elements</a>
    <a href="https://github.com/mimo84/bootstrap-maxlength" target="_blank" class="list-group-item list-group-item-action d-flex font-weight-bold">
    <span class="list-group-item-icon lgi-icon-bs"></span>
    Bootstrap Maxlength: Official documentation</a>
</div>

## Demo

{% capture example %}
<div class="form-group">
  <label for="maxlength1">Username</label>
  <input type="text" class="form-control" id="maxlength1" placeholder="Choose a username" maxlength="20">
</div>
<div class="form-group mt-4">
  <textarea class="form-control" id="maxlength2" placeholder="My limited textarea" maxlength="250"></textarea>
</div>
{% endcapture %}
{% include example.html content=example %}

## Tutorial

Import **Bootstrap Maxlength** after your Material javascripts.
{% highlight html %}
<script src="https://cdn.jsdelivr.net/npm/bootstrap-maxlength/dist/bootstrap-maxlength.min.js"></script>
{% endhighlight %}

Add a `maxlength` attribute to your input field.
{% highlight html %}
<textarea class="form-control" id="textareaExample" placeholder="Try this textarea" maxlength="250"></textarea>
{% endhighlight %}

Initialize plugin once. Here is an example of simplest declaration to be active on all inputs with maxlength attribute set.
{% highlight js %}
$('[maxlength]').maxlength({
  alwaysShow: true,
  warningClass: 'form-text text-muted',
  limitReachedClass: 'form-text text-muted',
  placement: 'bottom-right-inside'
})
{% endhighlight %}

All parameters are detailed in [official documentation](https://github.com/mimo84/bootstrap-maxlength).

That's it.