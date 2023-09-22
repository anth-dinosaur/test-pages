# {{ page.title }}

Here is a list of people from my YAML file:

{% for person in site.data.mydata %}
- **Name:** {{ person.name }}
- **Age:** {{ person.age }}
- **Occupation:** {{ person.occupation }}
{% endfor %}
