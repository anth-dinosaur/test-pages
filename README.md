# Test Page

> [!NOTE]  
> Highlights information that users should take into account, even when skimming.

> [!IMPORTANT]  
> Crucial information necessary for users to succeed.

> [!WARNING]  
> Critical content demanding immediate user attention due to potential risks.


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

[treeTest](treeTest.md)
