+++
title = "Sample post — the conventions baked into zola-quiet"
description = "Tour of the elements this theme styles: code blocks, addendum blocks, the xkcd shortcode, tags."
date = 2026-01-01

[taxonomies]
tags = ["sample", "conventions"]
+++

> Blockquote on the homepage looks like this — quiet, italic, with a
> left rule. Good for opening a post with a thesis or note.

A regular paragraph in the body. Inline code looks like `this`,
and a code block looks like:

```bash
echo "hello, quiet world"
```

```go
package main

import "fmt"

func main() {
    fmt.Println("hello")
}
```

The headings stay at weight 400 — that's the defining "quiet" trick
from Minima, and the terminal skin keeps a similar restraint with
all headings at the same size.

## &gt; lists

- Bulleted lists use the system bullet.
- The terminal skin replaces them with `→ ` arrows.
- Either way, no chrome.

1. Ordered lists work too.
2. Numbers stay tabular.

## &gt; the addendum block

When you want to add a note to a post after it's originally
published, wrap it in `<div class="addendum">…</div>`:

<div class="addendum">

<p class="addendum-eyebrow">Added — June 2026</p>

## &gt; an example addendum

This block sits inside the post but visibly differs from the
surrounding prose — left rule, tinted background, a small eyebrow
label noting when it was added. Useful for corrections, follow-ups,
or attaching an interactive visualiser to a post you wrote earlier.

</div>

## &gt; the xkcd shortcode

If you save `static/img/xkcd/<num>.png` and call:

```
{% raw %}{{ xkcd(num=1319, title="Automation", alt="…") }}{% endraw %}
```

…you get a `<figure class="xkcd">` with attribution to Randall and
the CC BY-NC 2.5 licence link. Removed the inline call above to
avoid a 404 in the demo build; uncomment when you ship the image.

## &gt; tags

The post's tags appear as quiet monospace chips below the body. Add
them in the front matter under `[taxonomies]`.
