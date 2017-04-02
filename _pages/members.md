---
layout: default
permalink: /members/
---
<div class="row">
  <div class="col-xs-12 h4">
    Raid Team Members
  </div>
</div>
{% for group in site.data.raiders.groups %}
  <div class="row">
    <div class="col-xs-12">
      <table class="table table-bordered">
        <caption>{{group.name}}</caption>
        <tr>
          <th>Name</th>
          <th>Class</th>
          <th>Spec</th>
          <th>Off-Spec</th>
        </tr>
        {% for raider in group.members %}
          <tr>
            <td>{{raider.name}}</td>
            <td>{{raider.class}}</td>
            <td>{{raider.spec}}</td>
            <td>
              {% if raider.offspec %}
                {{raider.offspec}}
              {% else %}
                N/A
              {% endif %}
            </td>
          </tr>
        {% endfor %}
      </table>
    </div>
  </div>
{% endfor %}
