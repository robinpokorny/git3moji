---
layout: default
---
<h2 class="no-anchor">
{% for item in site.data.git3moji.list %}{{item.emoji}}{% endfor %}
</h2>
<h1>
<a href="{{ site.baseurl }}">git3moji</a>
<small>v{{site.data.git3moji.version}}</small>
</h1>

*[git-three-**moh**-jee]*  is a simple three-letter (or less) **emoji standard for expressive commit messages**.

> *Warning:* Pre-release version. It exists to record the ideas and promote [discussion](https://github.com/robinpokorny/git3moji/issues).

[Introduction](#introduction) –
[List](#list) –
[FAQ](#faq) –
[About](#about)

---

{% include headline.html name="Introduction" slug="introduction" %}

Prepend one of the five emojis to describe the intention of your commit.

This is
[certainly](https://gitmoji.carloscuesta.me/)
[not](https://github.com/slashsBin/styleguide-git-commit-message)
a new idea. There are many long creative lists of recommended commit emojis. The problem is that “long” and “creative” isn’t good for the real world. Without compliance to some sort of standard with strict limits, emojis are useless in bigger teams. This project aims at providing such a lightweight set.

### Features
* **At the first sight** you can recognise purpose of a commit.
* **Three-letter (or less) codes** are easy to remember and quick to write. No more 📈 (`:chart_with_upwards_trend:`). This is where the `3` in the name comes from.
* **Small set of emojis** prevents time-consuming search for “the best fit”. Every team member can learn them by heart or peak at a credit card-sized cheat sheet.

### How to use
The selected emoji must be at the very beginning of the commit message.

Use the shorthand form with colons (`:`) surrounding the name. Do not include the emoji symbol itself as it could break in terminals and other legacy environments.

It is recommended to separate the emoji and the text description with a single space.

**Example**:

```bash
$ git commit -m ":zap: Add users endpoint, fixes #27"
```

Which would be displayed as:

```
1b74135 ⚡️ Add users endpoint, fixes #27
```

{% include headline.html name="List of emojis" slug="list" %}

Emoji| Code    | Description
---  |---      |---
{% for item in site.data.git3moji.list %}{{item.emoji}} | `{{item.code}}` | {{item.description}}
{% endfor %}

Get the list in the form of [JSON](https://raw.githubusercontent.com/robinpokorny/git3moji/master/_data/git3moji.json).

{% include headline.html name="FAQ" slug="faq" %}

#### Do we need a ‘specification’ for 5 emojis?

This document aims to be a reference point for teams and individuals who would like to categorise their commits by their intention.
It should also serve as a starting place for developers contributing to an adhering project.

Giving a bit of formal style should simplify the adoption and speed up the learning process. A shared specification has a higher chance of describing edge cases.

The actual number of emojis in the spec is somewhat irrelevant—fewer being a feature in this case, the same way as [SemVer](http://semver.org/) is not just ‘3 numbers’.

#### What if no emoji on the list suits my need? What if more emojis describe the commit?

As the number of emojis to choose from is deliberately low this scenario is probable. Please think again what is the main change in your commit, which files are mostly affected. Also consider splitting the commit into more smaller commits. If you still feel unsure, `:zap:` is likely one with the most general use.

It is tempting to introduce a new emoji. Please restrain to do so and keep the system simple and coherent.
If you truly believe there is a use case for extending the list, please [start a discussion](https://github.com/robinpokorny/git3moji/issues/).

#### Can I have more emojis in the commit message?

Of course! The remainder of the commit message is beyond the scope of this standard. You might want to introduce a team-specific rules about it. Adding more meaningful emojis can be beneficial.

You should be careful and not overwhelm readers with too many emojis. That would be confusing, which is exactly what we want to avoid. Similary emojis from this specification should not appear outside the beginning of the message.

In any case it is recommended to include a space (or other delimiter) after the emoji from the list. This helps visually distinguish its role.

#### What git hosts support emojis?

[GitHub](https://github.com/), [BitBucket](https://bitbucket.org/)<sup>\[[#5](https://github.com/robinpokorny/git3moji/issues/5)\]</sup>, and [GitLab](https://about.gitlab.com/) display shortcodes in commit messages as emojis.

#### Something missing? [Ask your question](https://github.com/robinpokorny/git3moji/issues)

{% include headline.html name="About" slug="about" %}
The *git3moji* specification is authored by [Robin Pokorny](https://robinpokorny.com/).
It adheres to [Semantic Versioning](http://semver.org/spec/v2.0.0.html).

If you’d like to leave feedback, please [open an issue](https://github.com/robinpokorny/git3moji/issues).

### Attribution
This project was inspired by [gitmoji](https://gitmoji.carloscuesta.me/), a project by [Carlos Cuesta](https://carloscuesta.me/), which felt overwhelming.

### License

<a href="http://creativecommons.org/publicdomain/zero/1.0/"><amp-img src="{{ site.baseurl }}/images/cc-zero.png" alt="CC0" height="31" width="88"></amp-img></a>

To the extent possible under law, authors have waived all copyright and related or neighboring rights to *git3moji*.
