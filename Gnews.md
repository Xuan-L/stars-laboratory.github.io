---
layout: page
title: "News"
permalink: /news/
main_nav: true
---

### Recent News and Updates

* August 2021: Dr. Liu's paper is featured in the Industrial and Systems Engineer magazine (ISE) Magazine. 
* August 2021: PhD student Zhangyue Shi presented his research works in the IDETC/CIE 2021 conference. He is partially supported by the student stipends from the ASME CIE division. 
* June 2021: PhD student Zhangyue Shi presented his research works in the NAMRC49/MSEC2021 conference. He is supported by the NSF-Sponsored Student Support Award. 
* May 2021: PhD student Yuxuan Li and Zhangyue successfully passed their PhD qualifying exam. Congratulations! 
* April 2021: Master student Ayse Dogan successfully defended her MS thesis. Congratulations! 
* April 2021: Dr. Liu was elected as a board director in data analytics and information systems (DAIS) division of IISE. 
* March 2021: Dr. Liu gave a seminar in the Department of Industrial and Manufacturing Engineering at North Dakota State University. 
* January 2021: PhD student Yuxuan Li won the Best Poster Award in the 5th International Workshop on Biomedical Informatics with Optimization and Machine Learning (BOOM) in Conjunction with 29th International Joint Conference on Artificial Intelligence (IJCAI). Congratulations! 
* November 2020: Our group gave multiple invited talks at 2020 Virtual INFORMS Annual Meeting. 
* October 2020: Our paper "A Blockchain-based G-code Protection Approach for Cyber-Physical Security in Additive Manufacturing" has been accepted by ASME Journal of Computing and Information Science in Engineering. 
* October 2020: Our paper "An Integrated Manifold Learning Approach for High Dimensional Data Feature Extractions and its Applications to Online Process Monitoring of Additive Manufacturing" has been accepted IISE Transactions. 
* March 2020: Undergraduate student Jackson Baker's paper, mentored by Dr. Liu, won the second place in the 2020 IISE Southcentral Regional Undergraduate Technical Paper Competition. Congratulations! 
* March 2020: Dr. Liu gave a seminar in the Department of Statistics at Oklahoma State University. 
* December 2019: The senior design team mentored by Dr. Liu won the IEM senior design poster competition. Congratulations! 
* October 2019: Our group gave multiple invited talks at INFORMS Annual Meeting, Seattle, 2019.  
* October 2019: Yuxuan and Zhangyue were selected as a finalist of 2019 INFORMS QSR Data Challenge Competition. Congratulations! 
* September 2019: Ayse Dogan joined our group as a new M.S. student. Welcome! 
* August 2019: Dr. Liu gave an invited talk at the 2019 Annual SFF Symposium. 
* August 2019: Yuxuan Li and Zhangyue Shi joined our group as new Ph.D. students. Welcome! 


{% for category in site.categories %}
  {% capture cat %}{{ category | first }}{% endcapture %}
  <h2 id="{{cat}}">{{ cat | capitalize }}</h2>
  {% for desc in site.descriptions %}
    {% if desc.cat == cat %}
      <p class="desc"><em>{{ desc.desc }}</em></p>
    {% endif %}
  {% endfor %}
  <ul class="posts-list">
  {% for post in site.categories[cat] %}
    <li>
      <strong>
        <a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
      </strong>
      <span class="post-date">- {{ post.date | date_to_long_string }}</span>
    </li>
  {% endfor %}
  </ul>
  {% if forloop.last == false %}<hr>{% endif %}
{% endfor %}
<br>
