---
Title: "{{title | escape}}"
Year: {{date | format("YYYY (MMMM)")}}
Authors: {{authors}}
Tags: 
{% for t in tags %}
- {{t.tag | replace(" ", "_")}}
{% endfor %}
aliases: 
- "{{title | escape}}"
- "{{shortTitle | escape}}"
---
{%- if abstractNote %}
> [!ABSTRACT]
>{{abstractNote}}
{%- endif %}
---
> [!tip] LINK
{% if pdfZoteroLink -%}
> {{pdfZoteroLink}}
{%- else -%}
> [LINK]({{desktopURI}}.md)
{% endif %}

{% for annotation in annotations -%}
{%- if annotation.annotatedText -%}
> [!note]
>{{annotation.annotatedText | safe | replace('<','') | replace('>','') }} 
{%- endif -%}
{%- if annotation.imageRelativePath -%} 
> [!important] Image
> ![[{{annotation.imageRelativePath}}]]
{% endif -%}
{% if annotation.imageRelativePath -%} 
> _{{annotation.comment | safe}} [Page {{annotation.pageLabel}}](zotero://open-pdf/library/items/{{annotation.attachment.itemKey}}?page={{annotation.pageLabel}}&annotation={{annotation.id}})_
{% else -%}
_{{annotation.comment | safe}} [Page {{annotation.pageLabel}}](zotero://open-pdf/library/items/{{annotation.attachment.itemKey}}?page={{annotation.pageLabel}}&annotation={{annotation.id}})_
{% endif -%}
---
{% endfor -%}