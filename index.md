---
title: Lexent Bio - Late Stage Study - Help Guide
link_name: Late Stage Study
order: 1
---

{% assign study = site.collections | where: "label", "late_stage_study_steps" | first %}
<!-- {% increment step_counter %}
{% increment new_step_counter %}
-->

# Study: {{ study.title }}
<hr/>
#### Help Topics
{% for step in study.docs %}
##### [{% increment step_counter %}. {{ step.title }}](#{{ step.id }})

{% endfor %}

{% for step in study.docs %}
<hr/>
<a name="{{ step.id }}"></a>
## {% increment new_step_counter %}. {{ step.title}}
{{ step.content }}
{% endfor %}
