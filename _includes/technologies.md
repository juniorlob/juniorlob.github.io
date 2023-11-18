<table>
  <thead>
    <tr>
      <th>{{i18n_config.general_info.technology}}</th>
      <th>{{ i18n_config.general_info.years_of_experience }}</th>
    </tr>
  </thead>
  <tbody>
    {% for technologie in data.technologies.list %}
      <tr>
        <td>{{ technologie.name }}</td>
        <td>{{ technologie.experience_years }}</td>
      </tr>
    {% endfor %}
  </tbody>
</table>
