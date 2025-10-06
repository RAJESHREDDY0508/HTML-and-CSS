<!--
  This repository is a collection of small projects built to practise core HTML and
  CSS skills.  A clear and informative README not only helps others understand
  what the repository contains but also acts as a guide for your future self.
  The following sections explain the structure of the project, demonstrate
  notable examples and include simple diagrams to visualise page layouts.
-->

# HTML and CSS Practice Repository

## Overview

This repository contains a variety of HTML pages with accompanying CSS files to
illustrate different web‑development concepts.  It starts with simple pages
that use headings, paragraphs, lists and buttons and gradually introduces more
advanced topics like **flexbox**, **grid layouts** and **positioning**.  The
most elaborate example is a miniature YouTube clone (`youtube.html`) that
combines many of these techniques: a fixed header with tooltips, a collapsible
sidebar and a responsive grid of video previews.  All
examples use plain HTML and CSS—no JavaScript or frameworks—so you can focus on
understanding how markup and styling work together.

## Repository structure

The repository is organised into directories by asset type.  Here is a
high‑level summary:

| Path                       | Description |
|---------------------------|------------|
| `index.html`              | A very basic page demonstrating headings, paragraphs, lists and buttons. |
| `youtube.html`            | A YouTube‑style landing page that brings together multiple CSS files and image assets. |
| `htmlFiles/`              | Contains standalone HTML examples such as **Buttons**, **Text**, **Flexbox**, **Grid** and **Position** demos. |
| `cssFiles/`               | CSS stylesheets used by the various HTML files.  The YouTube clone uses `generalyoutube.css`, `header.css`, `sidebar.css` and `video.css`. |
| `channel‑pictures/`       | JPEG profile images for the YouTube example. |
| `thumbnails/`             | `.webp` thumbnails used in the video grid on `youtube.html`. |
| `icons/`                  | SVG icons (menu, search, upload etc.) used throughout the YouTube page. |

Throughout this README you will see citations (e.g.) pointing back to the original code so you can jump to the relevant lines for more detail.

## Quick start

1. **Clone or download** the repository.  A local copy ensures that all
   relative links to CSS, images and icons work correctly.
2. **Open the files in your browser.**  You can double‑click any `.html`
   file to view it.  Start with `index.html` for a gentle introduction, then
   explore the examples in `htmlFiles/` and finish with `youtube.html`.
3. **Inspect the code.**  Open the corresponding files in a text editor to
   understand how HTML tags and CSS rules interact.  Each demo keeps the CSS
   separate from the HTML where possible, so you can easily modify styles
   without touching the markup.

### Tips for local development

- If you open `youtube.html` directly from the file system and the icons or
  thumbnails don’t appear, try serving the folder through a simple local
  server (for example, `python3 -m http.server` in the repository root) so
  that relative paths resolve correctly.
- Modern browsers offer developer tools (usually opened via <kbd>F12</kbd>)
  that let you inspect elements, view applied styles and experiment with
  layout properties interactively.

## Examples

### Basic HTML: `index.html`

The simplest example demonstrates how to structure a web page using headings,
paragraphs and lists.  Two buttons and a link show how
interactive elements look without any custom styling.  Use this file to
familiarise yourself with basic tags like `<h1>`, `<p>`, `<ul>`/`<li>`,
`<button>` and `<a>`.

### Buttons

There are two button exercises:

* **`htmlFiles/buttons.html` + `cssFiles/buttons.css`** – Shows how to
  create subscribe/join/tweet buttons reminiscent of social media platforms.
  The CSS demonstrates hover states and transitions.
* **`htmlFiles/Buttons_Practice.html` + `cssFiles/Buttons_Practice.css`** –
  Provides additional styles such as dark buttons that invert colours on hover
  and pill‑shaped call‑to‑action buttons with drop shadows.

Experiment with these files by tweaking colours, padding or border radius to
see how they affect the appearance and behaviour of buttons.

### Text formatting

Several pages explore text styling:

* **`htmlFiles/Text.html` + `cssFiles/text.css`** – Uses classes to style
  different types of text: a video title, view count, author name and a
  promotional banner.  You’ll
  learn about font families, sizes, line height, margins and hover effects on
  inline links.
* **`htmlFiles/Textexercise1.html` + `cssFiles/Textexercise1.css`** –
  Demonstrates how to use headings, subheadings and supporting text along
  with a call‑to‑action button styled in green.

### Layouts: Flexbox, Grid and Positioning

CSS layout systems are among the most powerful tools for web design.  This
repository includes small playgrounds to help you understand them:

* **Flexbox (`htmlFiles/flexbox.html`)** – Shows how to align items in
  rows, control their proportional widths using `flex` values and use
  properties like `justify-content` and `align-items` to space them out
  horizontally and vertically.  The example also
  demonstrates how margins and borders interact with flexible items.
* **Grid (`htmlFiles/grid.html`)** – Illustrates different `grid-template-columns`
  configurations: fixed pixel widths, fractional units (`1fr`) and responsive
  grids with gaps.  Notice how changing the column
  definition alters the layout of the boxes.
* **Positioning (`htmlFiles/position.html`)** – Uses `position: fixed` for
  sticky headers and sidebars, `position: relative` as a containing block and
  `position: absolute` for overlays like badges or timers.  You’ll also see how `z-index` controls stacking
  order.

Below is a simple diagram contrasting flexbox and grid layouts to aid your
intuition:

![Flexbox vs Grid]({{file:file-7oAxHxkzpRkXgXo6wg145P}})

### YouTube clone

The crown jewel of this repository is `youtube.html`, a simplified recreation
of YouTube’s home page.  It combines multiple concepts:

* A **fixed header** containing a hamburger menu, logo, search bar, voice
  search button and icons for upload, apps and notifications.
  Tooltips appear on hover thanks to absolutely positioned elements and
  `opacity` transitions defined in `cssFiles/header.css.
* A **vertical sidebar** with icons and labels; it stays fixed on the left
  side of the page and highlights links on hover.
* A **responsive grid** of video previews.  Each preview comprises a thumbnail,
  the channel’s profile picture and video metadata (title, author and views).
  Media queries in `cssFiles/video.css` adjust the number of columns based on
  the viewport width.

To help visualise the overall layout, the following diagram shows how the
header, sidebar and video grid fit together.  The colours are purely
representational and there is no actual content inside the blocks:

![YouTube layout diagram]({{file:file-5Gdsxu8Z2ZwijJW1kqUidS}})

When you open `youtube.html` locally, the page should resemble the basic
structure of YouTube’s home page, complete with thumbnails from the
`thumbnails/` directory and profile pictures from `channel‑pictures/`.  Feel
free to swap out the images or customise the CSS to make the page your own.

## Contributing

This repository is intended as a learning playground.  If you’d like to add
new examples (for instance, demonstrating CSS animations or responsive
navigation menus), feel free to fork the repository and submit a pull
request.  Contributions that expand on the concepts here are welcome.

## License

The content in this repository is provided for educational purposes.  Unless
otherwise stated, you may use, modify and distribute the code freely.
