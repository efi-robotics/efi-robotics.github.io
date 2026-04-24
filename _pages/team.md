---
layout: page
title: team
permalink: /team/
description: members of the lab
nav: false
nav_order: 5
---


<div class="team-grid">
  {% assign current_members = site.data.team.current %}
  {% for member in current_members %}
  <div class="team-member">
    <img src="{{ member.image }}" alt="{{ member.name }}" class="team-photo">
    <h4>{% if member.link and member.link != "" %}<a href="{{ member.link }}" target="_blank">{{ member.name }}</a>{% else %}{{ member.name }}{% endif %}</h4>
    <p class="role">{{ member.role }}</p>
    {% if member.supervisor and member.supervisor != "" %}
    <p><strong>Supervisor:</strong> {{ member.supervisor }}</p>
    {% endif %}
    {% if member.project and member.project != "" %}
    <p>{{ member.project }}</p>
    {% endif %}
  </div>
  {% endfor %}
</div>

---

<!-- ### co-supervision

<div class="team-grid">
  {% assign co_supervised_members = site.data.team.co_supervision %}
  {% for member in co_supervised_members %}
  <div class="team-member">
    <img src="{{ member.image }}" alt="{{ member.name }}" class="team-photo">
    <h4>{{ member.name }}</h4>
    <p class="role">{{ member.role }}</p>
    {% if member.supervisor and member.supervisor != "" %}
    <p><strong>Co-supervised with:</strong> {{ member.supervisor }}</p>
    {% endif %}
    {% if member.project and member.project != "" %}
    <p>{{ member.project }}</p>
    {% endif %}
  </div>
  {% endfor %}
</div>

--- -->

### current msc/meng students

{% assign msc_students = site.data.team.msc_students %}

<!-- MEng in Engineering Mathematics -->
{% assign meng_students = msc_students | where: "role", "MEng in Engineering Mathematics" | concat: msc_students | where_exp: "member", "member.role contains 'MEng Engineering Mathematics'" %}
{% if meng_students.size > 0 %}
<h4 class="alumni-category">MEng in Engineering Mathematics</h4>
<ul class="alumni-list">
  {% for member in meng_students %}
  <li>
    <strong>{{ member.name }}</strong>{% if member.project and member.project != "" %}, <em>{{ member.project }}</em>{% endif %}
  </li>
  {% endfor %}
</ul>
{% endif %}

<!-- MSc in Robotics -->
{% assign msc_robotics_current = msc_students | where: "role", "MSc in Robotics" %}
{% if msc_robotics_current.size > 0 %}
<h4 class="alumni-category">MSc in Robotics</h4>
<ul class="alumni-list">
  {% for member in msc_robotics_current %}
  <li>
    <strong>{{ member.name }}</strong>{% if member.project and member.project != "" %}, <em>{{ member.project }}</em>{% endif %}
  </li>
  {% endfor %}
</ul>
{% endif %}

<!-- MSc in Data Science -->
{% assign msc_data_science_current = msc_students | where: "role", "MSc in Data Science" %}
{% if msc_data_science_current.size > 0 %}
<h4 class="alumni-category">MSc in Data Science</h4>
<ul class="alumni-list">
  {% for member in msc_data_science_current %}
  <li>
    <strong>{{ member.name }}</strong>{% if member.project and member.project != "" %}, <em>{{ member.project }}</em>{% endif %}
  </li>
  {% endfor %}
</ul>
{% endif %}



<!-- <div class="team-grid">
  {% assign msc_students = site.data.team.msc_students %}
  {% for student in msc_students %}
  <div class="team-member">
    <img src="{{ student.image }}" alt="{{ student.name }}" class="team-photo">
    <h4>{{ student.name }}</h4>
    <p class="role">{{ student.role }}</p>
    {% if student.supervisor and student.supervisor != "" %}
    <p><strong>Supervisor:</strong> {{ student.supervisor }}</p>
    {% endif %}
    {% if student.project and student.project != "" %}
    <p>{{ student.project }}</p>
    {% endif %}
  </div>
  {% endfor %}
</div> -->

---

### alumni

{% assign alumni_members = site.data.team.alumni %}

<!-- PhD Alumni -->
{% assign phd_alumni = alumni_members | where: "role", "PhD" | sort: "year" | reverse %}
{% if phd_alumni.size > 0 %}
<h4 class="alumni-category">PhD</h4>
<ul class="alumni-list">
  {% for member in phd_alumni %}
  <li>
    <strong>{{ member.name }}</strong>{% if member.project and member.project != "" %}{% if member.link and member.link != "" %}, <em><a href="{{ member.link }}" target="_blank">{{ member.project }}</a></em>{% else %}, <em>{{ member.project }}</em>{% endif %}{% endif %} ({{ member.year }})
  </li>
  {% endfor %}
</ul>
{% endif %}

<!-- MEng in Engineering Mathematics -->
{% assign meng_alumni = alumni_members | where: "role", "MEng in Engineering Mathematics" | sort: "year" | reverse %}
{% if meng_alumni.size > 0 %}
<h4 class="alumni-category">MEng in Engineering Mathematics</h4>
<ul class="alumni-list">
  {% for member in meng_alumni %}
  <li>
    {% if member.link and member.link != "" %}<a href="{{ member.link }}" target="_blank"><strong>{{ member.name }}</strong></a>{% else %}<strong>{{ member.name }}</strong>{% endif %}{% if member.project and member.project != "" %}, <em>{{ member.project }}</em>{% endif %} ({{ member.year }})
  </li>
  {% endfor %}
</ul>
{% endif %}

<!-- Research Internships -->
{% assign internship_alumni = alumni_members | where_exp: "member", "member.role contains 'Internship'" | sort: "year" | reverse %}
{% if internship_alumni.size > 0 %}
<h4 class="alumni-category">Research Internships</h4>
<ul class="alumni-list">
  {% for member in internship_alumni %}
  <li>
    {% if member.link and member.link != "" %}<a href="{{ member.link }}" target="_blank"><strong>{{ member.name }}</strong></a>{% else %}<strong>{{ member.name }}</strong>{% endif %}{% if member.project and member.project != "" %}, <em>{{ member.project }}</em>{% endif %} ({{ member.year }})
  </li>
  {% endfor %}
</ul>
{% endif %}

<!-- MSc in Robotics -->
{% assign msc_robotics = alumni_members | where: "role", "MSc in Robotics" | sort: "year" | reverse %}
{% if msc_robotics.size > 0 %}
<h4 class="alumni-category">MSc in Robotics</h4>
<ul class="alumni-list">
  {% for member in msc_robotics %}
  <li>
    {% if member.link and member.link != "" %}<a href="{{ member.link }}" target="_blank"><strong>{{ member.name }}</strong></a>{% else %}<strong>{{ member.name }}</strong>{% endif %}{% if member.project and member.project != "" %}, <em>{{ member.project }}</em>{% endif %} ({{ member.year }})
  </li>
  {% endfor %}
</ul>
{% endif %}

<!-- MSc in Data Science -->
{% assign msc_data_science = alumni_members | where: "role", "MSc in Data Science" | sort: "year" | reverse %}
{% if msc_data_science.size > 0 %}
<h4 class="alumni-category">MSc in Data Science</h4>
<ul class="alumni-list">
  {% for member in msc_data_science %}
  <li>
    {% if member.link and member.link != "" %}<a href="{{ member.link }}" target="_blank"><strong>{{ member.name }}</strong></a>{% else %}<strong>{{ member.name }}</strong>{% endif %}{% if member.project and member.project != "" %}, <em>{{ member.project }}</em>{% endif %} ({{ member.year }})
  </li>
  {% endfor %}
</ul>
{% endif %}



<style>
.team-grid {
  display: grid;
  grid-template-columns: repeat(4, 250px); /* Default: 4 columns, each 250px wide */
  justify-content: center; /* Center the grid items horizontally */
  gap: 20px; /* Space between grid items */
  margin-top: 20px;
}

.team-member {
  text-align: center;
  border: 1px solid #ddd;
  padding: 15px;
  border-radius: 10px;
  background-color: #f9f9f9;
  height: 200px; /* Fixed height for uniformity */
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

.team-photo {
  width: 100px;
  height: 100px;
  border-radius: 50%;
  object-fit: cover;
  margin: 0 auto 10px;
}

.role {
  font-size: 0.9em;
  color: gray;
}

.alumni-list {
  margin-top: 20px;
  padding-left: 20px;
  list-style-type: disc;
}

.alumni-list li {
  margin-bottom: 10px;
}

.alumni-category {
  margin-top: 25px;
  margin-bottom: 12px;
  padding-bottom: 8px;
  border-bottom: 1px solid #e8e8e8;
  font-size: 0.95em;
  font-weight: 500;
  color: #666;
}

.alumni-category:first-of-type {
  margin-top: 30px;
}

/* Responsive Design */
@media (max-width: 1200px) {
  .team-grid {
    grid-template-columns: repeat(3, 250px); /* 3 columns for medium screens */
  }
}

@media (max-width: 768px) {
  .team-grid {
    grid-template-columns: repeat(2, 250px); /* 2 columns for smaller screens */
  }
}

@media (max-width: 480px) {
  .team-grid {
    grid-template-columns: repeat(1, 250px); /* 1 column for very small screens */
  }
}
</style>