---
layout: page
order: 1
title: Affiliated Event Schedule
sidebar: schedule_affiliatedevents
---

<button onclick="topFunction()" id="toTopButton" title="Go to top">Back to Top</button> 

Most affiliated events will take place the week before the Technical Symposium.

<strong>How to register for affiliated events</strong> : Affiliated events are events that occur in cooperation with the SIGCSE Technical Symposium, also using Pathable as the virtual platform.  <em>Symposium registration is required to attend any SIGCSE TS 2021 affilated event.</em>  See each individual affiliated event for information on registering.  Some events require prior application or submission.  For any questions related to affiliated events, please contact the organizers directly.

{% assign end_divs = "</div></div>" %}

{% for affiliatedevent in site.data.affiliatedevents.affiliatedevents %}
<div class="card">
<div class="container">
<h2 id="event-{{affiliatedevent.event | downcase}}">{{ affiliatedevent.title }}</h2>
<span class="alert-box papersession">{{ affiliatedevent.day }} / {{ affiliatedevent.time }}</span>
{% if affiliatedevent.url %}
<p><strong>Event website</strong> : <a href="{{affiliatedevent.url}}" target=_new>{{affiliatedevent.url}}</a></p>
{% endif %}
<p><strong>Event organizers</strong> : {{affiliatedevent.organizers}}</p>
<p><strong>Event contact</strong> : <a href="mailto:{{affiliatedevent.contact}}">{{affiliatedevent.contact}}</a></p>
<p><strong>How to register</strong> : {{affiliatedevent.register}}</p>
{% if affiliatedevent.submissions %}
<p><strong>Submissions</strong> : {{affiliatedevent.submissions}}</p>
{% endif %}
<p>{{affiliatedevent.description}}</p>
</div>
</div>
{% endfor %}