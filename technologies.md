<table>
  <thead>
    <tr>
      <th>Technology</th>
      <th>Years of experience</th>
    </tr>
  </thead>
  <tbody>
    {% for technologie in data.technologies %}
      <tr>
        <td>{{ technologie.name }}</td>
        <td>{{ technologie.experience_years }}</td>
      </tr>
    {% endfor %}
  </tbody>
</table>
