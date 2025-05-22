# Slideover Extension for Quarto Reveal.js Presentations

Adds content overlays that _slide over_ the existing slide to Quarto Revealjs presentations — hence the `.slideover` moniker.

This extension was created to overlay instructional content on Jupyter Notebooks and web apps in ValidMind's training portal. It provides a cleaner alternative to CSS modals that often interfere with the underlying content.

![Demonstration of slide-overs auto-collapsing and being manually toggled](slideover.gif)

## Demo

Try the [live demo](https://nrichers.github.io/slideover/) to see slideover in action.

## Features

- Works with [Quarto Revealjs presentations](https://quarto.org/docs/presentations/revealjs/)
- Slides over the presentation from the right or bottom
- Optional auto-collapse after 5 seconds
- Mobile responsive
- Supports basic text styling (bold, italic)
- Smooth animations and transitions

## Installation

You can install this extension using the following command:

```bash
quarto add nrichers/slideover
```

## Usage

To enable, add the extension to your YAML front matter:

```yaml
format:
  revealjs:
    revealjs-plugins: 
      - slideover
```

Then add a div with the `.slideover` class:

For bottom slide-overs, use `.slideover--b`:

```md
::: {.slideover--b}
This is an example that slides content over from the bottom.
:::
```

For auto-collapsing slide-overs, add the `.auto-collapse` class:

```md
::: {.slideover--b .auto-collapse}
This is an example that slides content over from the bottom and then auto-collapses after five seconds.
:::
```

```md
::: {.slideover--r}
This is an example that slides content over from the right.
:::
```

## Tips & Tricks

- Slideover provides basic styling support for **bold** and _italic_ text
- For advanced styling, use [Tachyons Extension For Quarto](https://github.com/nareal/tachyons)
- Headings are NOT supported inside slideovers due to Quarto and Pandoc limitations

## License

MIT licensed. Copyright (C) 2025 Nik Richers.
