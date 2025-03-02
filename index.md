---
layout: default
title: "Arunkumar Thangasamy"
---

# About Me  
**Name:** {{ site.name }}  
**Email:** [{{ site.email }}](mailto:{{ site.email }})  
**Phone:** {{ site.phone }}  
**LinkedIn:** [Profile]({{ site.linkedin }})  

## Education  
{% for edu in site.education %}
- **{{ edu.degree }}**  
  *{{ edu.university }}*  
  GPA: {{ edu.gpa }}  
  ({{ edu.duration }})  
{% endfor %}

## Skills  
- **Programming Languages:** {{ site.skills.languages | join: ", " }}  
- **Design & Simulation Tools:** {{ site.skills.design_simulation | join: ", " }}  
- **Project Management Tools:** {{ site.skills.project_tools | join: ", " }}  
- **Analytics & Data Tools:** {{ site.skills.analytics_tools | join: ", " }}  
- **Soft Skills:** {{ site.skills.soft_skills | join: ", " }}  

## Experience  
{% for job in site.experience %}
- **{{ job.role }}** at **{{ job.company }}** ({{ job.duration }})  
  {% for task in job.responsibilities %}
  - {{ task }}  
  {% endfor %}
{% endfor %}

## Certifications  
{% for cert in site.certifications %}
- {{ cert }}
{% endfor %}

## Projects  
{% for project in site.projects %}
- **{{ project.name }}**: {{ project.description }}
{% endfor %}
