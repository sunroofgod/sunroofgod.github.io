# Sunroofgod Portfolio Website [![CI](https://github.com/sunroofgod/sunroofgod.github.io/actions/workflows/hugo.yaml/badge.svg)](https://github.com/sunroofgod/sunroofgod.github.io/actions/workflows/hugo.yaml/badge.svg)

A [Hugo](https://gohugo.io/)-theme based on a fork of [Hugo ʕ•ᴥ•ʔ Bear Blog](https://github.com/janraasch/hugo-bearblog).

## Installation

Clone repo

```bash
git clone git@github.com:sunroofgod/sunroofgod.github.io.git
```

For more information, read the official [setup guide][hugo-setup-guide] of Hugo.

## Content

### Stickies

You can add **a new sticky note** by running

```bash
./create -s "<Title of Note>"
```

- `title` and `description` defined in sticky notes do not contribute to note on UI. 
- `tags` functionality for sticky notes are still a **work-in-progress**. 
  - adding tags to notes will result in unexpected behaviour when viewing them

### Blog

You can add **a new blog post** by running

```bash
./create -b "<Title of Blog Post>"
```

### Others

You can add **a new page** by running

```bash
./create -p "<Title of Page>"
```

## Development
Run the static site locally via

```bash
hugo server -D
```