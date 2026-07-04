---
title: Configuration
nav_order: 2
---

# Configuration
{: .no_toc }

Just the Docs has some specific configuration parameters that can be defined in your Jekyll site's \_config.yml file.
{: .fs-6 .fw-300 }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

View this site's [\_config.yml](https://github.com/just-the-docs/just-the-docs/tree/main/_config.yml) file as an example.

## Site logo

```yaml
# Set a path/url to a logo that will be displayed instead of the title
logo: "/assets/images/just-the-docs.png"
```

## Site favicon

```yaml
# Set a path/url to a favicon that will be displayed by the browser
favicon_ico: "/assets/images/favicon.ico"
```

If the path to your favicon is `/favicon.ico`, you can leave `favicon_ico` unset.

## Search

```yaml
# Enable or disable the site search
# Supports true (default) or false
search_enabled: true

search:
  # Split pages into sections that can be searched individually
  # Supports 1 - 6, default: 2
  heading_level: 2
  # Maximum amount of previews per search result
  # Default: 3
  previews: 3
  # Maximum amount of words to display before a matched word in the preview
  # Default: 5
  preview_words_before: 5
  # Maximum amount of words to display after a matched word in the preview
  # Default: 10
  preview_words_after: 10
  # Set the search token separator
  # Default: /[\s\-/]+/
  # Example: enable support for hyphenated search words
  tokenizer_separator: /[\s/]+/
  # Display the relative url in search results
  # Supports true (default) or false
  rel_url: true
  # Enable or disable the search button that appears in the bottom right corner of every page
  # Supports true or false (default)
  button: false
  # Focus the search input by pressing `ctrl + focus_shortcut_key` (or `cmd + focus_shortcut_key` on macOS)
  focus_shortcut_key: 'k'
```

## Mermaid Diagrams
{: .d-inline-block }

New (v0.4.0)
{: .label .label-green }

The minimum configuration requires the key for `version` ([from jsDelivr](https://cdn.jsdelivr.net/npm/mermaid/)) in `_config.yml`:

When *all* your pages are in a single collection, its name is not displayed.

The navigation for each collection is a separate name space for page titles: a page in one collection cannot be a child of a page in a different collection, or of a normal page.
