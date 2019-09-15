---
title: David S. Hayden
layout: home
---

<table border="0" cellpadding="0">
<td valign="top" style="min-width:140px;">
<img src="/assets/david.jpg" width="160">
</td>
<td valign="top">
PhD Candidate<br/>
Computer Science and Artificial Intelligence Laboratory<br/>
Department of Electrical Engineering and Computer Science<br/>
Massachusetts Institute of Technology<br/>
<a href="mailto:dshayden@mit.edu">dshayden@mit.edu</a><br/>
<a href="/assets/dshayden-cv.pdf">Curriculum Vitae</a>
</td>
</table>

Short Bio

<h2 class="tableheading">Publications</h2>

<table border="0">
  {% for pub_keyval in site.data.publications %}
    <tr>
      {%- assign pub = pub_keyval[1] -%}
      <td>
        <b><a href="{{pub_keyval[0]}}.html" style="color: #464646">{{ pub.title }}</a></b><br/>
        {%- for author in pub.authors -%}
          {%- if forloop.last == true and forloop.length > 1 %}
            and
          {%- endif %}
          {%- if author == "kjolstad" %}
            <font color="#000000">{{ site.data.authors[author].name }}</font>
          {%- else %}
            <a href="{{- site.data.authors[author].site -}}" style="color: #464646">{{ site.data.authors[author].name }}</a>
          {%- endif -%}
          {%- if forloop.last == false and forloop.length > 2 -%}
            ,
          {%- endif %}
        {%- endfor -%}<br/>
        <i>{{ pub.venue }}
        {%- if pub.venuenote %}
        ({{ pub.venuenote }})
        {%- endif -%}
        {%- if pub.volume -%}
        , Volume {{ pub.volume }}
        {%- endif -%}
        {%- if pub.issue -%}
        , Issue {{ pub.issue }}
        {%- endif -%}
        </i>, {{ pub.month }} {{ pub.year }}<br/>
        {%- if pub.award -%}
          <i><b>{{ pub.award }}</b></i><br/>
        {%- endif -%}
      </td>
      <td valign="top" width="20">
        {% if pub.pdf %}
          <a href="{{ pub.pdf }}"><img src="/assets/pdf.png" alt="pdf" /></a>
        {% endif %}
        {% if pub.movie %}
          <a href="{{ pub.movie }}"><img src="/assets/movie.png" alt="youtube" /></a>
        {% endif %}
      </td>
    </tr>
{% endfor %}
</table>


<h2 class="tableheading">Press</h2>

<table border="0">
{%- for press_keyval in site.data.press %}
  {%- assign press= press_keyval[1] -%}
  <tr>
  <td> 
    <b><a href="{{press.url}}">{{press.title}}</a></b><br/>{{press.venue}}
  </td>
  </tr>
{% endfor %}
</table>

