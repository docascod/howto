# Metadata

You can use several ways to add metadata on your document

## Header

````markdown
---
title: 'document title: with subtitle'
keywords: [example, output.slides]
author: 
- docsascode
lang: en-EN
myparam: 'Local Param'
---

your document
````

## External metadata

Metadata can be stored in external YAML ou JSON file.

This file can be set in document header :

````markdown
extra_meta: relative/path/to/your/metafile
````

Or just add a file with the same name as your document but with extra extension `.meta`. Example : `yourdocument.md` and `yourdocument.md.meta`

## Attributes

Metadata can be used with placeholder :

````markdown
The following strings have been substitued with **{myparam}**
````

or in conditional bloc :

````markdown
<!-- ifeval "{myparam}" == "Local Param" -->
This is a conditional block
<!-- end_ifeval -->

<!-- ifeval "{myparam}" == "value" -->
This is a conditional block (not match)
<!-- end_ifeval -->

<!-- ifdef myparam -->
Available only if myparam is defined
<!-- end_ifdef -->

<!-- ifndef myparam -->
Available only if myparam is ** NOT** defined
<!-- end_ifndef -->
````