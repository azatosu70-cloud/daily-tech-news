# ITニュースレポート

{% assign reps = site.pages | where_exp: "p", "p.path contains 'reports/'" | sort: "path" | reverse %}
{% for p in reps %}- [{{ p.path | remove: 'reports/' | remove: '.md' }}]({{ p.url | relative_url }})
{% endfor %}
