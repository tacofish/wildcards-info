---
layout: default
title: Members
permalink: /members/
---
<div class="row">
  <div class="col-xs-12 h4">
    Raid Team Members
  </div>
</div>

<div class="row">
  <div class="col-xs-12">
    <table class="table table-bordered" id="members">
      <thead>
        <tr>
          <th>Name</th>
          <th>Class</th>
          <th>Spec</th>
          <th>Off-Spec</th>
          <th>Rank</th>
        </tr>
      </thead>
      <tfoot>
        <tr>
          <th>Name</th>
          <th>Class</th>
          <th>Spec</th>
          <th>Off-Spec</th>
          <th>Rank</th>
        </tr>
      </tfoot>
      <tbody>
      {% for raider in site.data.raiders %}
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
          <td>{{raider.rank}}</td>
        </tr>
      {% endfor %}
      </tbody>
    </table>
  </div>
</div>
