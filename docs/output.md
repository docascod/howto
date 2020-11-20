 # Choose your output

`output` is the key ! With `output` you can choose theme and configuration for you final document. DAC comes with 3 outputs : document, slides and note.

`output.document` generates a book like document

`output.slides` generates slides

`output.note` generates lightweight document (as note)

## Configure output

Desired output must be set into document metadata with `keywords` key. 

?> You can set one or more output. If you don't choose one, default is `output.document`

Example in [markdown](md_meta.md) :

````markdown
---
keywords: [output.slides, output.document]
---

document content
````

By this way, also you can select company theme.

````markdown
---
keywords: [output.slides, output.document, output.document.mycompany]
---

document content
````

## DAC output comparison

| **keyword**     | **Format** | **Orientation** | **Size** | **Title page** | **Table of content** |
| --------------- | :--------: | :-------------: | :------: | :------------: | :------------------: |
| output.document |    PDF     |    portrait     |    A4    |      yes       |         yes          |
| output.slides   |    PDF     |    landscape    |   Wide   |      yes       |          no          |
| output.note     |    PDF     |    portrait     |    A4    |       no       |          no          |



