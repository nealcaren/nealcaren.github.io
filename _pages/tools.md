---
layout: page
permalink: /tools/
title: tools
description: Tools I use.
nav: true
nav_order: 6
---

Here are some tools I use. I'm putting them here so I can stop Googling them every time I need a command.

## Download YouTube videos

```bash
uv tool install yt-dlp   --upgrade
uvx yt-dlp -f best -o "video.mp4" "https://www.youtube.com/watch?v=u2cB-9uM90Y"
```

## LLM assisted coding for free

```bash
aider --model gemini/gemini-exp-1206
```

## Summary details about a CSV file

Produces a report in Markdown format. Useful for understanding and telling an LLM the structure of a CSV file.

```bash
uv tool install describecsv
describecsv sample.csv
```

## OCR a modern PDF to Markdown

```
uv tool install docling
docling some.pdf --from pdf --to md --image-export-mode placeholder
```

### EPUB to Markdown using Pandoc

```bash
pandoc sample.epub -t gfm-raw_html --wrap=none   -o sample.md
```

## Build a Python app and release to PyPI

```bash
python3 -m build
python3 -m twine upload dist/*
```