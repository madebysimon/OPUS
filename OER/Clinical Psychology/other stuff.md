---
layout: default
title: Frontmatter Stuff
nav_order: 2
parent: Clinical Psychology
---

# Test One
blablabla

This is a child-page (see frontmatter "parent")

# Aux links for the upper right navigation
aux_links:
  "Just the Docs on GitHub":
    - "//github.com/pmarsceill/just-the-docs"


# Navigation Structure
{: .no_toc }
This heading does not show up in TOC



layout: default
title: Frontmatter Stuff
nav_order: 2
nav_exclude: true
parent: A
has_toc: false


Contribute and see all authors on our → github

---
 this is the parent page - see frontmatter

# hello world
Welcome to my first note
## this is H2
### and this is H3

😄 this is an emoji and [^1]

[^1]: a footnote


| asdasd | asdasd |
| --- | --- |
| 1 | 2 |

> this is a blockquote

```
this is code
```

1. list item one
2. list item two
	1. two one
	2. two two

- something
	- something else

---

[Link button](http://example.com/){: .btn }

[Link button](http://example.com/){: .btn .btn-purple }
[Link button](http://example.com/){: .btn .btn-blue }
[Link button](http://example.com/){: .btn .btn-green }

[Link button](http://example.com/){: .btn .btn-outline }

---

<span class="fs-8">
[Link button](http://example.com/){: .btn }
</span>

<span class="fs-3">
[Tiny ass button](http://example.com/){: .btn }
</span>

[Button with space](http://example.com/){: .btn .btn-purple .mr-2 }
[Button ](http://example.com/){: .btn .btn-blue }

[Button with more space](http://example.com/){: .btn .btn-green .mr-4 }
[Button ](http://example.com/){: .btn .btn-blue }


---

#bts
{: .label }

Blue label
{: .label .label-blue }

Stable
{: .label .label-green }

New release
{: .label .label-purple }

Coming soon
{: .label .label-yellow }

Deprecated
{: .label .label-red }


---

<div class="code-example" markdown="1">

[Link button](http://example.com/){: .btn }

</div>
```markdown
[Link button](http://example.com/){: .btn }
```