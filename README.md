# Resume theme

_Resume_ is a theme for creating professional resumes with [Cecil](https://cecil.app).

![Demo screenshot](docs/screenshot.png)

## Features

- One page resume: contact, about, profiles and work experiences
- Work experiences managed as pages, sorted by start date
- Empty sections are hidden
- Localization ready (english and french)

## Installation

```bash
composer require cecil/theme-resume
```

> Or [download the latest archive](https://github.com/Cecilapp/theme-resume/releases/latest/) and uncompress its content in `themes/resume`.

## Usage

Add `resume` in the `theme` section of your configuration file:

```yaml
theme:
  - resume
```

The homepage (`pages/index.md`) content is displayed in the _About_ section.

### Configuration

```yaml
title: John Doe
baseline: Senior Full Stack Developer # optional
description: John Doe, Senior Full Stack Developer based in Lyon, France.
resume:
  contact: # each entry is optional
    email: john.doe@example.com
    phone: +33 1 99 00 12 34
    website: https://johndoe.example.com
  profiles:
    - network: GitHub
      username: johndoe # optional
      url: https://github.com/johndoe # optional
```

### Work experiences

Create _work experiences_ pages in `pages/works/` (e.g. `pages/works/nimbus-labs.md`):

```markdown
---
company: Nimbus Labs # optional, fallback to title
position: Senior Full Stack Developer # optional
url: https://nimbuslabs.example.com # optional
start: 2018-03-01 # required
end: 2021-08-31 # optional, "Present" if not set
---
Core developer of a SaaS platform for managing field service teams.

- Built the public REST API and its OpenAPI documentation
- Moved infrastructure to AWS using Terraform
```

See the [`demo`](demo/) folder for a complete example.

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
