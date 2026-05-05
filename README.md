# samsinn-pack-nuclear

A samsinn pack that surfaces the **Nuclear Wiki** — a knowledge base
on AI agent systems for nuclear operations.

This pack is **thin metadata**. The wiki content lives at
[samsinn-wikis/nuclear-wiki](https://github.com/samsinn-wikis/nuclear-wiki)
and renders at https://samsinn-wikis.github.io/nuclear-wiki/. samsinn
links to it; it does not download or cache pages.

## Install

In a running samsinn instance:

```
install_pack samsinn-packs/samsinn-pack-nuclear
```

Then activate the pack in any room where the link should appear
(Settings → Packs → toggle `nuclear` for the room).

The wiki link will show up in the Packs panel. Agents can suggest
"see the Nuclear Wiki at <url>"; if they need to actually read a page,
they can use the built-in `web_fetch` tool against the rendered URL.

## What's in the manifest

```json
{
  "name": "nuclear",
  "wikis": [
    { "name": "Nuclear Wiki", "url": "https://samsinn-wikis.github.io/nuclear-wiki/" }
  ]
}
```

That's it.

## History

Originally bundled wiki content was published in this repo. Replaced
with thin metadata in v0.2.0 (samsinn commit N) — content stays in
its source repo where it can be viewed + edited normally.
