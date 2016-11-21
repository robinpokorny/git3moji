---
layout: default
---
## {% for item in site.data.git3moji.list %}{{item.emoji}}{% endfor %}
<h1>
<a href="./">git3moji</a>
<small>v{{site.data.git3moji.version}}</small>
</h1>

*[git-three-**moh**-jee]*  is a short **emoji standard for expressive commit messages**.

> *Warning:* Pre-release version. It exists to record the ideas and promote [discussion](https://github.com/robinpokorny/git3moji/issues).

<!-- @TODO
[Introduction](#introduction) –
[List](#list-of-emojis) –
[FAQ](#faq) –
[About](#about)
-->
---

## Introduction

Prepend one of the five emojis to describe the intention of your commit.

This is
[certainly](https://gitmoji.carloscuesta.me/)
[not](https://github.com/slashsBin/styleguide-git-commit-message)
a new idea. There are many long creative lists of recommended commit emojis. The problem is that “long” and “creative” isn’t good for the real world. Without compliance to some sort of standard with strict limits, emojis are useless in bigger teams. This project aims at providing such a lightweight set.

### Features
* **At the first sight** you can recognise purpose of a commit.
* **Three-letter (or less) codes** are easy to remember and quick to write. No more 📈 (`:chart_with_upwards_trend:`). This is where the `3` in the name comes from.
* **Small set of emojis** prevents time-consuming search for “the best fit”. Every team member can learn them by heart or peak at a credit card-sized cheat sheet.

## List of emojis

Emoji| Code    | Description
:---:|:---:    |:---
{% for item in site.data.git3moji.list %}{{item.emoji}} | `{{item.code}}` | {{item.description}}
{% endfor %}

Get the list in the form of [JSON](https://raw.githubusercontent.com/robinpokorny/git3moji/master/_data/git3moji.json).

<!-- @TODO
## Usage
`git commit -m ":zap: Add users endpoint, fixes #27"`
`1b74135 ⚡️ Add users endpoint, fixes #27`
-->

## About
The *git3moji* specification is authored by [Robin Pokorny](https://robinpokorny.com/).
It adheres to [Semantic Versioning](http://semver.org/spec/v2.0.0.html).

If you’d like to leave feedback, please [open an issue](https://github.com/robinpokorny/git3moji/issues).

### Attribution
This project was inspired by [gitmoji](https://gitmoji.carloscuesta.me/), a project by [Carlos Cuesta](https://carloscuesta.me/), which felt overwhelming.

### License

<a href="http://creativecommons.org/publicdomain/zero/1.0/">
  <img src="./images/cc-zero.png" width="88">
</a>

To the extent possible under law, authors have waived all copyright and related or neighboring rights to *git3moji*.
