---
layout: default
---
{%- assign data = site.data.data %}

## {{data.title}}

{{ data.description }}
---

## Experience

{% for experience in data.experience %}

### {{ experience.professional_title }}

### [{{ experience.company }}]({{ experience.company_url }}) - ({{ experience.period }})

{% if experience.technologies %}
  **Technologies:** {{experience.technologies | join: ', '}}
{% endif %}

{{ experience.description }}

{% if experience.internal_experiences %}
  {% for internal_experiences in experience.internal_experiences %}

#### {{ internal_experiences.title }}

{% if internal_experiences.technologies %}
  **Technologies:** {{internal_experiences.technologies | join: ', '}}
{% endif %}

{{ internal_experiences.description }}
{% if forloop.last == false %}
---
{% endif %}

{% endfor %}
{% endif %}

{% if forloop.last == false %}
---
{% endif %}

{% endfor %}

## Technologies
{% include_relative technologies.md %}

## Education and Certificates

{% for education in data.education %}
  {{ education.institution }} - {{ education.period }} \
  {{ education.course }} - {{ education.degree }} | {{ education.status }}
{% endfor %}
