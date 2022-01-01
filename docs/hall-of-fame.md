---
layout: default
title: Hall of Fame
nav_order: 9000
permalink: /halloffame
has_children: false
info: data is in `_data/halloffame.yml`, css in `_sass/custom/custom.scss`
---

# [Codeforces](https://codeforces.com/)

<div class="HOF-table">
<table class="HOF">
<tr>
  <th>Name</th>
  <th>Handle</th>
  <th>Peak Rating</th>
  <th>Title</th>
</tr>
{% for user in site.data.halloffame.codeforces %}
{% if user.r >= 2600 %}
  {% assign col = "cf-IGM" %}
  {% assign utitle = "International Grandmaster" %}
{% elsif user.r >= 2400 %}
  {% assign col = "cf-GM" %}
  {% assign utitle = "Grandmaster" %}
{% elsif user.r >= 2300 %}
  {% assign col = "cf-IM" %}
  {% assign utitle = "International Master" %}
{% elsif user.r >= 2200 %}
  {% assign col = "cf-M" %}
  {% assign utitle = "Master" %}
{% endif %}
<tr>
  <td>{{user.name}}</td>
  <td><a href="https://codeforces.com/profile/{{ user.u }}" class="handle {{col}}">{{user.u}}</a></td>
  <td><div class="handle {{col}}">{{ user.r }}</div></td>
  <td><div class="handle {{col}}">{{ utitle }}</div></td>
</tr>
{% endfor %}
</table>
</div>

# [AtCoder](https://atcoder.jp/)

<div class="HOF-table">
<table class="HOF">
<tr>
  <th>Name</th>
  <th>Handle</th>
  <th>Peak Rating</th>
  <th>Title</th>
</tr>
{% for user in site.data.halloffame.atcoder %}
{% if user.r >= 2400 %}
  {% assign col = "ac-dan3" %}
  {% assign utitle = "Dan 3" %}
{% elsif user.r >= 2200 %}
  {% assign col = "ac-dan2" %}
  {% assign utitle = "Dan 2" %}
{% elsif user.r >= 2000 %}
  {% assign col = "ac-dan1" %}
  {% assign utitle = "Dan 1" %}
{% elsif user.r >= 1800 %}
  {% assign col = "ac-kyu1" %}
  {% assign utitle = "Kyu 1" %}
{% endif %}
<tr>
  <td>{{user.name}}</td>
  <td><a href="https://atcoder.jp/users/{{ user.u }}" class="handle {{col}}">{{user.u}}</a></td>
  <td><div class="handle {{col}}">{{ user.r }}</div></td>
  <td><div class="handle">{{ utitle }}</div></td>
</tr>
{% endfor %}
</table>
</div>

# [Codechef](https://www.codechef.com/)

<div class="HOF-table">
<table class="HOF">
<tr>
  <th>Name</th>
  <th>Handle</th>
  <th>Peak Rating</th>
  <th>Title</th>
</tr>
{% for user in site.data.halloffame.codechef %}
{% if user.r >= 2500 %}
  {% assign col = "cc-7" %}
  {% assign utitle = "7&#9733;" %}
{% elsif user.r >= 2200 %}
  {% assign col = "cc-6" %}
  {% assign utitle = "6&#9733;" %}
{% endif %}
<tr>
  <td>{{user.name}}</td>
  <td><a href="https://www.codechef.com/users/{{ user.u }}" class="handle {{col}}">{{user.u}}</a></td>
  <td><div class="handle {{col}}">{{ user.r }}</div></td>
  <td><div class="handle {{col}}">{{ utitle }}</div></td>
</tr>
{% endfor %}
</table>
</div>

# [Topcoder](https://community.topcoder.com/tc?module=AlgoRank)

<div class="HOF-table">
<table class="HOF">
<tr>
  <th>Name</th>
  <th>Handle</th>
  <th>Peak Rating</th>
</tr>
{% for user in site.data.halloffame.topcoder %}
{% if user.r >= 2200 %}
  {% assign col = "tc-red" %}
{% elsif user.r >= 1500 %}
  {% assign col = "tc-yellow" %}
{% endif %}
<tr>
  <td>{{user.name}}</td>
  <td><a href="https://www.topcoder.com/members/{{ user.u }}" class="handle {{col}}">{{user.u}}</a></td>
  <td><div class="handle {{col}}">{{ user.r }}</div></td>
</tr>
{% endfor %}
</table>
</div>

<hr/>
\* denotes currently active
