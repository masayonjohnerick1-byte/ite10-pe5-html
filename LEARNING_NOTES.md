# Beginner code notes - PE5 HTML

Use these notes to study the project, then close them and explain the ideas in your own words. The professor may ask you to demonstrate understanding, so change some recipe content and test what happens yourself.

## How an HTML page is organized

- `<!doctype html>` tells the browser to use modern HTML. `<html lang="en">` identifies the page language for browsers and assistive technology.
- The `<head>` contains information about the page, such as its character encoding, mobile viewport setting, title, description, and favicon. The `<body>` contains the content people see.
- `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<figure>`, and `<footer>` describe the purpose of parts of the page. They are more meaningful than using `<div>` for every element.
- Each page has one main `<h1>`. Heading levels organize the content; they are not chosen just to make text look large.

## Links, images, and paths

- A link such as `href="recipes/lemon-herb-pasta.html"` is a relative path. The browser looks for that file inside this project. On a recipe page, `../index.html` means go up one folder and open the homepage.
- `src="images/lemon-pasta.jpg"` connects an image to its local file. The `alt` text describes the visible picture for someone who cannot see it. It should not pretend that a stock photograph shows ingredients that are not visible.
- Image source notes and license references are in `images/SOURCES.md`.

## Lists, tables, forms, and audio

- `<ul>` is for a group without a required order, such as ingredients. `<ol>` is for steps where order matters.
- A `<table>` is for data arranged in rows and columns. Its `<caption>` describes the table; `<th scope="col">` and `<th scope="row">` identify headers for screen readers.
- A `<label for="recipe-choice">` is connected to a control whose `id` matches. `<fieldset>` and `<legend>` group the rating options. `required` asks the browser to check that the visitor made a choice.
- The feedback form uses `method="get"` and opens the local `thanks.html` page. It is a learning demo: it does not save or send responses to a server.
- `<audio controls>` gives the browser's built-in play/pause controls. The adjacent audio description gives the cue's content in text. `preload="metadata"` avoids autoplay and keeps loading light.

## Plain HTML and running the site

- No stylesheet or JavaScript is used. The browser displays the HTML with its ordinary default presentation.
- Open `index.html`, or start a local server in this folder using `python -m http.server 8000` and visit `http://localhost:8000`.
- All photos and the WAV audio file are local. The pages should still show assets when there is no network connection, except the external links listed in source notes.

## Check your understanding

Try explaining, without reading this page: why ingredients use an unordered list; why a method uses an ordered list; how a relative path works; what `alt` text is for; and why the local form does not send feedback. Then make one small change, reload the page, and describe what changed.
