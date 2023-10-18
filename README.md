# Resume theme

The _Resume_ theme for [Cecil](https://cecil.app) (***WIP***).

![Demo screenshot](docs/screenshot.png)

## Installation

```bash
composer require cecil/theme-resume
```

> Or [download the latest archive](https://github.com/Cecilapp/theme-resume/releases/latest/) and uncompress its content in `themes/resume`.

## Usage

Add `resume` in the `theme` section of your `config.yml`:

```yaml
theme:
  - resume
```

Configuration:

```yaml
title: John Doe
baseline: Programmer
description: John Doe, Full Stack Developer Ninja Expert.
resume:
  contact:
    email: john@doe.tld
    phone: +33 0 00 00 00 00
    website: https://johndoe.tld
  profiles:
    - network: Github
      username: JohnDoe
      url: https://github.com/JohnDoe
```

Creates _work experiences_ pages in `pages/works`:

```yaml
---
company: Company
position: "Job #1"
url: https://company.tld
start: 2015-01-01
---
Job description.
```

### Internationalization

This theme support [localization](https://cecil.app/documentation/templates/#localization), and provides french (`fr_FR`) translation (see `translations/messages.fr_FR.po`).

Configuration:

```yaml
languages:
  - code: fr
    locale: fr_FR
```

## License

 _Resume_ is a free software distributed under the terms of the MIT license.

© [Arnaud Ligny](https://arnaudligny.fr)
