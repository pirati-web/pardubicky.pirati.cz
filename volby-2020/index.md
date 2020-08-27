---
layout: elections-2020
title: Krajské volby 2020
heroBgImg: articles/2020/kampan20/zahajenikampan.jpg
campaignGroupUid: volby-2020
campaignCategoryUid: kraj2020
candidateListUid: kraj2020
customizeHeader: true
---

{% assign candidates = site.candidatelists | where: "uid", page.candidateListUid | first %}

{% capture mainContent %}
  <h1 class="head-alt-lg md:head-alt-xl text-center">Krajské volby 2020</h1>
{% endcapture %}

{% capture subContent %}
  <h2 class="head-xs md:head-base mt-2 text-center">Šance <strong>změnit budoucnost</strong></h2>
{% endcapture %}

{% include elections-header.html img=page.img bgImg=page.heroBgImg mainContent=mainContent subContent=subContent candidateListNumber=candidates.number %}

