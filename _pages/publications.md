---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

{% include base_path %}

<style>
.journal-title {
  color: #4EACE9; /* Change this color to whatever you prefer */
}
</style>

## Textbook Chapters

- **Artificial intelligence for materials spectroscopy**  
  *Authors: Steven B. Torrisi, John M. Gregoire, Junko Yano, Matthew R. Carbone, Carla P. Gomes, Linda Hung, Santosh K. Suram*  
  *Published in: "Accelerated Materials Discovery: How to Use Artificial Intelligence to Speed Up Development," Chapter 3, edited by Phil De Luna, 2022, De Gruyter, Berlin, Boston.*  
  [Link to Chapter](https://doi.org/10.1515/9783110738087-003)

## Publications 

{% assign sorted_publications = site.data.publications.publications | sort: 'year' | reverse %}
{% assign count = sorted_publications.size %}
<ol reversed>
{% for publication in sorted_publications %}
  <li>
    <strong>{{ publication.title }}, <span class="journal-title">{{ publication.journal }}</span>, {{ publication.year }}</strong>  
    <br><em>Authors: {{ publication.authors }}</em>  
    <br><em>Published in {{ publication.journal }}, vol. {{ publication.volume }}, no. {{ publication.number }}, {{ publication.pages }}.</em>
    {% assign count = count | minus: 1 %}
  </li>
{% endfor %}
</ol>