---
layout: page
# title: HKU Systems Group Events
---

<!-- # Events

Welcome to the events page of the HKU Systems Group. Here you can find information about past and upcoming events, seminars, and workshops.

## Upcoming Events

{% assign upcoming_events = site.events | where_exp: "event", "event.date >= site.time" | sort: 'date' %}
{% if upcoming_events.size > 0 %}
<ul>
  {% for event in upcoming_events %}
  <li>
    <a href="{{ event.url }}">{{ event.title }}</a> - {{ event.date | date: "%B %d, %Y" }}
    <p>{{ event.description }}</p>
  </li>
  {% endfor %}
</ul>
{% else %}
<p>No upcoming events at the moment. Check back later!</p>
{% endif %} -->

## Past Events

{% assign past_events = site.events | where_exp: "event", "event.date < site.time" | sort: 'date' | reverse %}
{% if past_events.size > 0 %}
<ul>
  {% for event in past_events %}
  <li>
    <a href="{{ event.url }}">{{ event.title }}</a> - {{ event.date | date: "%B %d, %Y" }}
    <!-- <p>{{ event.description }}</p> -->
  </li>
  {% endfor %}
</ul>
{% else %}
<p>No past events.</p>
{% endif %}
