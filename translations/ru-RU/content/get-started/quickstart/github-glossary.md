---
title: GitHub glossary
intro: 'This glossary introduces common Git and {% data variables.product.prodname_dotcom %} terminology.'
redirect_from:
  - /articles/github-glossary
  - /github/getting-started-with-github/github-glossary
  - /github/getting-started-with-github/quickstart/github-glossary
versions:
  fpt: '*'
  ghes: '*'
  ghae: '*'
  ghec: '*'
---

{% for term in site.data.glossaries.external %}
  ### {% data glossaries.external[forloop.index0].term %}
  {% data glossaries.external[forloop.index0].description %}
  ---
{% endfor %}

---

## Дополнительная литература

- [The Official Git Glossary](https://www.kernel.org/pub/software/scm/git/docs/gitglossary.html)
- [Git Reference](http://gitref.org/)
- [Git SCM](https://git-scm.com/doc)
