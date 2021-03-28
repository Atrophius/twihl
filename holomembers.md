---
layout: page
title: Hololive Members
permalink: /holomem/
---

{% for member in site.data.holomem %}
### {{ member[1].name }} ({{ member[1].gen }})
{% if member[1].youtube %}[YouTube]({{ member[1].youtube }}) &middot;{% endif %}{% if member[1].twitter %} [Twitter]({{ member[1].twitter }}) &middot;{% endif %}{% if member[1].art_tag %} [Fan Art](https://twitter.com/hashtag/{{ member[1].art_tag }}){% endif %}
{% endfor %}

### Mega Art Feeds
{% capture mega_art_gen0 %}
{% for member in site.data.holomem %}{% if member[1].gen == "0th Gen" %}{% if member[1].art_tag %} OR #{{ member[1].art_tag }}{% endif %}{% endif %}{% endfor %}
{% endcapture %}
{% capture mega_art_gen1 %}
{% for member in site.data.holomem %}{% if member[1].gen == "1st Gen" %}{% if member[1].art_tag %} OR #{{ member[1].art_tag }}{% endif %}{% endif %}{% endfor %}
{% endcapture %}
{% capture mega_art_gen2 %}
{% for member in site.data.holomem %}{% if member[1].gen == "2nd Gen" %}{% if member[1].art_tag %} OR #{{ member[1].art_tag }}{% endif %}{% endif %}{% endfor %}
{% endcapture %}
{% capture mega_art_gamers %}
{% for member in site.data.holomem %}{% if member[1].gen == "Gamers" %}{% if member[1].art_tag %} OR #{{ member[1].art_tag }}{% endif %}{% endif %}{% endfor %}
{% endcapture %}
{% capture mega_art_gen3 %}
{% for member in site.data.holomem %}{% if member[1].gen == "3rd Gen" %}{% if member[1].art_tag %} OR #{{ member[1].art_tag }}{% endif %}{% endif %}{% endfor %}
{% endcapture %}
{% capture mega_art_gen4 %}
{% for member in site.data.holomem %}{% if member[1].gen == "4th Gen" %}{% if member[1].art_tag %} OR #{{ member[1].art_tag }}{% endif %}{% endif %}{% endfor %}
{% endcapture %}
{% capture mega_art_gen5 %}
{% for member in site.data.holomem %}{% if member[1].gen == "5th Gen" %}{% if member[1].art_tag %} OR #{{ member[1].art_tag }}{% endif %}{% endif %}{% endfor %}
{% endcapture %}
{% capture mega_art_id %}
{% for member in site.data.holomem %}{% if member[1].gen contains "ID" %}{% if member[1].art_tag %} OR #{{ member[1].art_tag }}{% endif %}{% endif %}{% endfor %}
{% endcapture %}
{% capture mega_art_en %}
{% for member in site.data.holomem %}{% if member[1].gen == "HoloMyth" %}{% if member[1].art_tag %} OR #{{ member[1].art_tag }}{% endif %}{% endif %}{% endfor %}
{% endcapture %}
{% capture mega_art_stars %}
{% for member in site.data.holomem %}{% if member[1].gen contains "Holostars" %}{% if member[1].art_tag %} OR #{{ member[1].art_tag }}{% endif %}{% endif %}{% endfor %}
{% endcapture %}
{% capture mega_art_managers %}
{% for member in site.data.holomem %}{% if member[1].gen contains "Manager" %}{% if member[1].art_tag %} OR #{{ member[1].art_tag }}{% endif %}{% endif %}{% endfor %}
{% endcapture %}

[Mega Fan Art Feed: Gen 0](https://twitter.com/search?q=({{ mega_art_gen0 | remove_first: "OR" | strip | url_encode }}))  
[Mega Fan Art Feed: Gen 1](https://twitter.com/search?q=({{ mega_art_gen1 | remove_first: "OR" | strip | url_encode }}))  
[Mega Fan Art Feed: Gen 2](https://twitter.com/search?q=({{ mega_art_gen2 | remove_first: "OR" | strip | url_encode }}))  
[Mega Fan Art Feed: Gamers](https://twitter.com/search?q=({{ mega_art_gamers | remove_first: "OR" | strip | url_encode }}))  
[Mega Fan Art Feed: Gen 3](https://twitter.com/search?q=({{ mega_art_gen3 | remove_first: "OR" | strip | url_encode }}))  
[Mega Fan Art Feed: Gen 4](https://twitter.com/search?q=({{ mega_art_gen4 | remove_first: "OR" | strip | url_encode }}))  
[Mega Fan Art Feed: Gen 5](https://twitter.com/search?q=({{ mega_art_gen5 | remove_first: "OR" | strip | url_encode }}))  
[Mega Fan Art Feed: ID](https://twitter.com/search?q=({{ mega_art_id | remove_first: "OR" | strip | url_encode }}))  
[Mega Fan Art Feed: EN](https://twitter.com/search?q=({{ mega_art_en | remove_first: "OR" | strip | url_encode }}))  
[Mega Fan Art Feed: Holostars](https://twitter.com/search?q=({{ mega_art_stars | remove_first: "OR" | strip | url_encode }}))  
[Mega Fan Art Feed: Managers](https://twitter.com/search?q=({{ mega_art_managers | remove_first: "OR" | strip | url_encode }}))