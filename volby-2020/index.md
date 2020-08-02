---
layout: communal-elections
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

<div class="container container--default">
  <h1 class="head-alt-md text-center pt-8 pb-2 lg:pt-24">Jsme s vámi</h1>
  <h2 class="head-xs text-center pb-8">Objíždíme všechny obce Pardubického kraje</h2>
</div>

<div style="-webkit-overflow-scrolling: touch; overflow-y: scroll;">
  <iframe class="lg:hidden" style="overflow: hidden; width: 100%; height: 300px;" allow="geolocation *; camera *;" frameborder="0" src="https://www.mapotic.com/grand-tour-piratu-pardubickeho-kraje/embed"></iframe>
  <iframe class="hidden lg:block" style="overflow: hidden; width: 100%; height: 480px;" allow="geolocation *; camera *;" frameborder="0" src="https://www.mapotic.com/grand-tour-piratu-pardubickeho-kraje/embed"></iframe>
</div>
