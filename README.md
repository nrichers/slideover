# Slideover Extension for Quarto Revealjs Presentations

This extension provides collapsible content overlays that slide over the existing slide. It was originally created to overlay instructional content on Jupyter Notebooks and web apps. The extension offers a cleaner alternative to static CSS modals, which often interfere with the underlying content.

![Demonstration of slide-overs auto-collapsing and being manually toggled](slideover.gif)

## Demo

Try the [live demo](https://nrichers.github.io/slideover/) to see slideover in action.

## Features

- Works with [Quarto Revealjs presentations](https://quarto.org/docs/presentations/revealjs/)
- Slides over the presentation from the right or bottom
- Optional auto-collapse after 5 seconds
- Mobile responsive

## Installation

Install the extension with:

```bash
quarto add nrichers/slideover
```

## Usage examples

To enable, add the extension to your YAML front matter:

```yaml
format:
  revealjs:
    revealjs-plugins: 
      - slideover
```

Then add a slideover:

```md
::: {.slideover--b}
Slides content over from the bottom.
:::
```


```md
::: {.slideover--b .auto-collapse}
Slides content over from the bottom and then auto-collapses after five seconds.
:::
```

```md
::: {.slideover--b .auto-collapse-10}
Slideover from the bottom that auto-collapses after 10 seconds.
:::
```


```md
::: {.slideover--r}
Slides content over from the right.
:::
```

```md
::: {.slideover--l}
Slides content over from the left.
:::
```

```md
::: {.slideover--t}
Slides content over from the top.
:::
```

## Tips & Tricks

- Slideover provides basic styling support for **bold** and _italic_ text
- For advanced styling, use [Tachyons Extension For Quarto](https://github.com/nareal/tachyons)
- Headings have special meaning in Quarto Revealjs presentations and are NOT supported inside slideovers.

## License

MIT licensed. Copyright (C) 2025 Nik Richers.
