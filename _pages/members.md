---
layout: default
permalink: /members/
---
# Raid Team List
{% for group in site.data.raiders.groups %}
- {{group.name}}
  {% for raider in group.members %}- {{raider.name}}
      - Class: {{raider.class}}
      - Main Spec: {{raider.spec}}
      {% if raider.offspec %}- Off Spec: {{raider.offspec}}{% endif %}
  {% endfor %}
{% endfor %}
