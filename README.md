# Test Page

## Occupations
{% assign unique_occupations = site.data.testdata | map: "occupation" | uniq %}
{% for occupation in unique_occupations %}
- [{{ occupation }}](#{{ occupation | slugify }})
{% endfor %}

{% for occupation in unique_occupations %}
## {{ occupation }}
{% for person in site.data.testdata %}
{% if person.occupation == occupation %}
- **Name:** {{ person.name }}
- **Age:** {{ person.age }}
{% endif %}
{% endfor %}
{% endfor %}

[TestTree](testTree.md)
