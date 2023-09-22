# Test Page

Here is a list of people from my YAML file:

{% for person in site.data.testdata %}
- **Name:** {{ person.name }}
- **Age:** {{ person.age }}
- **Occupation:** {{ person.occupation }}
{% endfor %}
