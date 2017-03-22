# hugo-default-theme

Concept for a default Hugo theme 

# Features

- [ ] basic settings in config file
- [ ] basic i18n
- [ ] menus
- [ ] blog
    - [ ] taxonomies
    - [ ] archetypes
    - [ ] next/prev
    - [ ] tag cloud
    - [ ] comments
- [ ] shortcodes (built-in and custom)
- [ ] color scheme choice
- [ ] code commenting for newbies

# Standards

- How to write a theme README
- config.toml
    + no trailing slash for `baseurl`
        * causes issues with .LanguagePrefix
        * paths should have slashes between each part, e.g. `{{ .Site.BaseURL }}/css/style.css` instead of `{{ .Site.BaseURL }}css/style.css`
    + Multilingual ready, so have both `languageCode` and `defaultContentLanguage`
    + emojify set?
    + google analytics set?
- site structure
    + themes should use `baseof.html`, even simple themes as this will make it easier for people to modify themes
    + head partials
        * complex head partials should have subdirectories, `partials/head/foo-bar`
        * styles, seo, rss, etc. -- if there are a lot, they can each get their own partial, e.g. `partials/head/metadata-rss.html`
- archetypes
    + default, post, and page all with sane front matter -- can make switching themes easier
- data
    + show how to use data with a relevant example
- static
    + image paths should be standardized to make switching themes easier
    + anything else that should be standardized to make switching themese easier?
- shortcodes
    + are there any that should be standardized that aren't built-in?
- Multilingual
    + keep a database of translated common strings people can use?
    + use `absLangURL` and `relLangURL` in templates instead of `absURL` and `relURL`
