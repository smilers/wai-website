---
title: "Tables Tutorial"
permalink: /tutorials/tables/
ref: /tutorials/tables/
lang: en

description:
image: /content-images/tutorials/tables/social.png
github:
  label: wai-tutorials

resource_title: Tables Tutorial

metafooter: true
last_updated: 2023-02-16
editors:
  - Eric Eggert: "https://www.w3.org/People/yatil/"
  - Shadi Abou-Zahra: "https://www.w3.org/People/shadi/"
update_editors:
  - Brian Elton
contributing_participants:
  - see <a href="/WAI/tutorials/acknowledgements/">Acknowledgements</a>
support: Developed by the Education and Outreach Working Group (<a href="https://www.w3.org/groups/wg/eowg">EOWG</a>). Developed with support from the <a href="https://www.w3.org/WAI/ACT/">WAI-ACT project</a>, co-funded by the <strong>European Commission <abbr title="Information Society Technologies">IST</abbr> Programme</strong>.


resource:
  ref: /tutorials/
navigation:
  next: /tutorials/tables/one-header/

wcag_success_criteria:
- 1.3.1
---

Data tables are used to organize data with a logical relationship in grids. Accessible tables need HTML markup that indicates header cells and data cells and defines their relationship. Assistive technologies use this information to provide context to users.

Header cells must be marked up with `<th>`, and data cells with `<td>` to make tables accessible. For more complex tables, explicit associations may be needed using `scope`, `id`, and `headers` attributes.

This tutorial shows you how to apply appropriate structural markup to tables. It includes the following pages:

{% include ednote.html note="Images need to be adapted to new icon styles eventually" %}

- {:.left} **[Tables with one header{% include image.html src="tutorials/tables/img-simple.png" class="small" %}](/tutorials/tables/one-header/)** for rows or columns: For tables with content that is easy to distinguish, mark up header cells with `<th>` and data cells with `<td>` elements.

- {:.left} **[Tables with two headers{% include image.html src="tutorials/tables/img-multidir.png" class="small" %}](/tutorials/tables/two-headers/)** have a simple row header and a simple column header: For tables with unclear header directions, define the direction of each header by setting the `scope` attribute to `col` or `row`.

- {:.left} **[Tables with irregular headers{% include image.html src="tutorials/tables/img-irreg.png" class="small" %}](/tutorials/tables/irregular/)** have header cells that span multiple columns and/or rows: For these tables, define column and row groups and set the range of the header cells using the `colgroup` and `rowgroup` values of the scope attribute.

- {:.left} **[Tables with multi-level headers{% include image.html src="tutorials/tables/img-multi.png" class="small" %}](/tutorials/tables/multi-level/)**  have multiple header cells associated per data cell:  For tables that are so complex that header cells can’t be associated in a strictly horizontal or vertical way, use `id` and `headers` attributes to associate header and data cells explicitly.

- {:.left} **[Caption & Summary{% include image.html src="tutorials/tables/img-caption.png" class="small" %}](/tutorials/tables/caption-summary/):** A caption identifies the overall topic of a table and is useful in most situations. A summary provides orientation or navigation hints in complex tables.
{:.nolist.withicons style="--img-width: 120px"}

Some document formats other than HTML, such as PDF, provide similar mechanisms to markup table structures. Word processing applications may also provide mechanisms to markup tables. Tables markup is often lost when converting from one format to another, though some programs may provide functionality to assist converting table markup.

Many web authoring tools and content management systems (CMS) provide functions to define header cells during table creation without having to edit the code manually.

{::nomarkdown}
{% include box.html type="start" title="Note" class="simple notes" %}
{:/}

This tutorial provides guidance for creating tables used to display data in a grid. This tutorial does not apply to tables used for layout. As a general rule, tables aren't meant to be used for layout purposes. Instead, a best practice is to use Cascading Style Sheets (CSS) for visual presentation.

{::nomarkdown}
{% include box.html type="end" %}
{:/}

## Why is this important?

Tables without structural markup to differentiate and properly link between header and data cells, create accessibility barriers. Relying on visual cues alone is not sufficient to create an accessible table. With structural markup, headers and data cells can be programmatically determined by software, which means that:

-   **People using screen readers** can have the row and column headers read aloud as they navigate through the table. Screen readers speak one cell at a time and reference the associated header cells, so the reader doesn’t lose context.

-    **Some people use alternative ways to render the data**, for example by using custom stylesheets to display header cells more prominently. Techniques like this enable them to change text size and colors and display the information as lists rather than grids. The table code needs to be properly structured to allow alternative renderings.
