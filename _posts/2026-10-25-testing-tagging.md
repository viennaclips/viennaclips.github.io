---
layout: post
title: "Testing author tagging"
date: 2026-10-25 10:00:00
author: Dominik Roth
tags: [meta]
tagged: [Dominik Roth, Your Name]
excerpt: "A quick test post to verify that tagged people show up with their avatars on cards and on the post page."
---

This post exists to test the **people tagging** feature.

If you can see avatars at the bottom of this post's card on the homepage, and a "with Dominik Roth · Your Name" row below the header on this page — tagging works.

## How to use it

Add an optional `tagged:` list to a post's header, with names exactly as they appear in `_data/authors.yml`:

```yaml
---
layout: post
title: "My post"
author: Dominik Roth
tagged: [Dominik Roth, Your Name]
---
```

- `tagged:` is **optional** — posts without it look exactly as before.
- Each tagged person needs an entry in `_data/authors.yml` so their photo resolves; unknown names fall back to the initials avatar.
- Tagged avatars link to the person's section on the Authors page, same as author chips.
