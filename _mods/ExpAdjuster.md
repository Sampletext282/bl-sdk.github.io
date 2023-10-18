---
layout: main

authors: "plu5" # Authors of the mod
title: Exp Adjuster # Title of the mod
version: "1.0.0 2021-04-05" # Version of the mod
supported: "BL2" # Supported games; currently can only display as "BL2", "BL2 + TPS", or "TPS"

tagline: "Sliders to adjust XP amounts on the fly." # A short description of the mod itself.
description: "Sliders to adjust XP amounts on the fly." # This is set in order to keep the SEO proper
longDescription: "Adds sliders to adjust XP amounts:\n- baserates for each mode,\n- as well as multipliers based on level difference from killed enemies.\n\nBy default all the values are set to what they are normally. Check Options -&gt; Mods menu to adjust them." # Description of what the mod can do
categories: ['Utility'] # Category of the type of mod

requirements: [] # Requirements for the given mod
requirementTitles: [] # The link-friendly name of the requirements

issues: "https://github.com/plu5/p-borderlands/issues"
download: "https://github.com/plu5/p-borderlands/releases/latest"
source: "https://github.com/plu5/p-borderlands/blob/main/ExpAdjuster" # Link to source code
license: [] # License name, link about the license from https://choosealicense.com/

---
**Contents**
* TOC
{:toc}

## {{page.title}}

Mod by: {{page.authors}}
Current Version: {{page.version}}

<p></p>
### Description

{{page.longDescription | markdownify }}

Currently Supports: `{{page.supported}}`

{% if page.categories.size > 0 %}
Categories:
{% for category in page.categories %}
  * [{{category}}](/types/{{category}})
{% endfor %}
<p></p>
{% endif %}

{% if page.requirements.size > 0 %}
### Requirements

{% for requirement in page.requirements %}

{% assign reqName = page.requirementTitles[forloop.index0] %}

{% for mod in site.mods %}

{% assign modName = mod.path | remove_first: '_mods/' %}
{% assign xz = reqName | append: '.md' %}

{% if modName == xz %}
* [{{ requirement }}]( {{ reqName | relative_url | prepend: '/mods'}} ) <sup>[(Direct Download)]({{mod.download}})</sup>
{% endif %}
{% endfor %}

{% endfor %}
<p></p>
{% endif %}

### Links

{% if page.download != "" %}
You can download {{page.title}} here: [Download Link]({{page.download}})
{% endif %}

{% if page.issues != "" %}
Report issues here: [Issue Tracker]({{page.issues}})
{% endif %}

{% if page.source != "" %}
View the source code here: [Source Code]({{page.source}})
{% endif %}

{% if page.license.size > 0 %}
This mod is licensed using {{page.license[0]}} <sup>[?]({{page.license[1]}})</sup>
{% endif %}