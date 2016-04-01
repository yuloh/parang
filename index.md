---
layout: default
---

# Introduction

This is a Jekyll theme for project documentation on github pages.  It uses the [skeleton](getskeleton.com) css framework for layout and default styling.

# Usage

## Repository Meta

Parang automatically pulls [repository metadata](https://help.github.com/articles/repository-metadata-on-github-pages/) to populate as much information as possible automatically.  Locally a [jekyll plugin](https://github.com/jekyll/github-metadata) is used for a seamless editing experience.

## Writing

Documentation is written in standard github flavoured markdown.  You can view a cheat sheet [here](https://help.github.com/articles/basic-writing-and-formatting-syntax/)  to learn the syntax.

## Code

Code blocks are written [just like on github](https://help.github.com/articles/creating-and-highlighting-code-blocks/).

Code highlighting uses the rouge syntax highlighter, which is the only syntax highlighter supported by github pages and the default for Jekyll 3.  Since code is highlighted when your site is built by jekyll, javascript isn't required to render it.  You can change the color scheme with one line in `_config.yml`.

```php
<?php

$deref  = new Yuloh\JsonGuard\Dereferencer();
$schema = $deref->dereference('http://json-schema.org/draft-04/schema#');

$data = json_decode('{ "id": "yuloh.dev/schema#" }');

$validator = new Yuloh\JsonGuard\Validator($data, $schema);

if ($validator->fails()) {
    $errors = $validator->errors();
}
```

```json
[
  {
    "code": 50,
    "message": "'yuloh.dev\/schema#' is not a valid uri.",
    "path": "\/id"
  }
]
```