---
layout: page
title: teaching
rank: 40
permalink: /courses/
description: My selected teaching experiences, including the courses I either teached or TAed. Refer to my CV for more information
nav: true
---

<div class="news">
  {% if site.courses != blank -%} 
    <div class="table-responsive">
      <table class="table table-sm table-borderless">
      {%- assign courses = site.courses | sort: "date" | reverse -%}
      {% for item in courses -%} 
        <tr align="left">
          <th scope="row">
            <h6><abbr class="badge font-weight-bold danger-color-dark text-uppercase align-middle">
              {{ item.semester }}
            </abbr></h6>
          </th>
          <td>
            <h5> {{ item.name }} </h5>
            🏫  {{ item.university }} <br>
            📌  {{ item.role}} <br>
            📚  {% for id in item.course_id %} 
                  {% if forloop.last %}
                    {{ id }}
                  {% else %}
                    {{ id }}, 
                  {% endif %}
                {% endfor %} <br>
            🧑‍🎓  {{ item.audience }} <br>
            {{ item.comment }} <br>
          </td>
        </tr>
      {%- endfor %} 
      </table>
    </div>
  {%- else -%} 
    <p>No courses provided...</p>
  {%- endif %} 
</div>


