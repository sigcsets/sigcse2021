---
layout: page
title: "For Attendees"
meta_title: "Information for Attendees for SIGCSE TS 2021"
permalink: "/attendees/"
sidebar: attendees
---

<a name="registration"></a>

## Registering for SIGCSE TS 2021

Registration for the 2021 SIGCSE Technical Symposium will open in early January 2021.

<style>
table tbody tr.odd, table tbody tr.alt, table tbody tr:nth-of-type(odd) {
    background-color: inherit;   /* reset rule in table.sccs */
}

table tbody:only-child tr.odd, table tbody:only-child tr.alt, table tbody:only-child tr:nth-of-type(odd) {
    background-color: #CCC;
}

table.multibody tbody:nth-child(odd) {
  background-color: #CCC;
}

th {
  text-align: center;
}

span.team-heading {
  font-size: 1.1rem;
}

</style>


### Registration Rates

{% for rate_category in site.data.registration.rates %}
  <h3>{{ rate_category[0] }}</h3>
  <table width="100%" class="multibody">
    <tr><th scope="col">Registration Type</th><th scope="col">Early: <br>{{site.data.registration.dates.early}}</th><th scope="col">Regular: <br>{{site.data.registration.dates.regular}}</th><th scope="col">On-site: <br>{{site.data.registration.dates.day-of}}</th></tr>
    <tbody>
    {% for rate_type in rate_category[1] %}
      <tr><td>{{ rate_type[0] }}</td><td>{{ rate_type[1].early }}</td><td>{{ rate_type[1].regular }}</td><td>{{ rate_type[1].day-of }}</td></tr>
    {% endfor %}
    </tbody>
  </table>
  
{% endfor %}