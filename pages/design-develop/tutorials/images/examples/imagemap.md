---
title: "Complete Image Maps Example"
permalink: /tutorials/images/examples/imagemap/
backlink: /tutorials/images/imagemap/an-organizational-chart-with-links-to-individual-pages
lang: en
description:
image: /content-images/tutorials/images/social.png
github:
  label: wai-tutorials

metafooter: true
last_updated: 2018-08-01
editors:
  - Eric Eggert: "https://www.w3.org/People/yatil/"
  - Shadi Abou-Zahra: "https://www.w3.org/People/shadi/"
update_editors:
  - Brian Elton
contributing_participants:
  - see <a href="/WAI/tutorials/acknowledgements/">Acknowledgements</a>
support: Developed by the Education and Outreach Working Group (<a href="https://www.w3.org/groups/wg/eowg">EOWG</a>). Developed with support from the <a href="https://www.w3.org/WAI/ACT/">WAI-ACT project</a>, co-funded by the <strong>European Commission <abbr title="Information Society Technologies">IST</abbr> Programme</strong>.
---


{::nomarkdown}
{% include box.html type="start" title="Example" class="example" %}
{:/}

![Board of directors and related staff: ]({{ "/content-images/tutorials/images/orgchart.png" | relative_url }}){:usemap="#Map"}

<map name="Map" id="Map">
  <area shape="rect" coords="176,14,323,58" href="../res/beyond" alt="Davy Jones: Chairman">
  <area shape="rect" coords="81,75,226,114" href="../res/beyond" alt="Carole Brewster: Company Secretary">
  <area shape="rect" coords="6,138,155,182" href="../res/beyond" alt="Harry H Brown: Marketing Director (reports to chairman)">
  <area shape="rect" coords="175,138,323,182" href="../res/beyond" alt="Paula Holbein: Sales Director (reports to chairman)">
  <area shape="rect" coords="345,136,496,186" href="../res/beyond" alt="Hugh Howard: Finance Director (reports to chairman)">
</map>

{::nomarkdown}
{% include box.html type="end" %}
{:/}

{::nomarkdown}
{% include box.html type="start" title="Code" class="example" %}
{:/}

~~~ html

<img src="orgchart.png"
     alt="Board of directors and related staff: "
     usemap="#Map">

<map name="Map" id="Map">
  <area
    shape="rect"
    coords="176,14,323,58"
    href="…"
    alt="Davy Jones: Chairman"
  >

  <area
    shape="rect"
    coords="81,75,226,114"
    href="…"
    alt="Carole Brewster: Company Secretary"
  >
  <area
    shape="rect"
    coords="6,138,155,182"
    href="…"
    alt="Harry H Brown: Marketing Director (reports to chairman)"
  >
  <area
    shape="rect"
    coords="175,138,323,182"
    href="…"
    alt="Paula Holbein: Sales Director (reports to chairman)"
  >
  <area
    shape="rect"
    coords="345,136,496,186"
    href="…"
    alt="Hugh Howard: Finance Director (reports to chairman)"
  >
</map>

~~~

{::nomarkdown}
{% include box.html type="end" %}
{:/}

