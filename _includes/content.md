


## {{data.title}}

{{ data.description }}
---

## {{ data.experience.title }}

{% for experience in data.experience.list %}

### {{ experience.professional_title }}

{% if experience.company_url %}
### [{{ experience.company }}]({{ experience.company_url }}) - ({{ experience.period }})
  {% else %}
### {{ experience.company }} - ({{ experience.period }})

{% endif %}

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

## {{ data.technologies.title }}
{% include technologies.md %}

## {{ data.education.title }}

{% for education in data.education.list %}
  {{ education.institution }} - {{ education.period }} \
  {{ education.course }} - {{ education.degree }} | {{ education.status }}
{% endfor %}
