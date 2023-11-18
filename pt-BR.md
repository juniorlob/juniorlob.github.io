---
layout: default
lang: pt-br
permalink: /pt-br
document: /assets/doc/Jair-Raiol-Lobo-Junior-PT-BR.pdf
---

{%-  assign lang = page.lang  %}
{%- assign data =  site.data[lang].owner_info %}
{%- assign i18n_config = site.data[lang].i18n-config %}

{% include content.md %}
