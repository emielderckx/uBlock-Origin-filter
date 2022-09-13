# uBlock-Origin-filter
Filters to block and remove copycat-websites from DuckDuckGo, Google and other search engines. Used to be specific to websites like StackOverflow or GitHub, but it currently supports others like Wikipedia.

To use this tools, you should have [uBlock Origin installed](https://github.com/gorhill/uBlock).

## Import into uBlock Origin

Select the filters flavors you want, depending on your needs and search engine:

💻 **`minecraft`** the original Minecraft-oriented filter

|          |                                                                                                                                                                                              Minecraft                                                                                                                                                                                              |
|-------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------:|
| Google            |                 [![uBO - add this filter](https://img.shields.io/static/v1?label=uBO&message=add%20this%20filter&color=de3f32&style=flat&logo=uBlock%20Origin)](https://subscribe.adblockplus.org/?location=https%3A%2F%2Fraw.githubusercontent.com%2Femielderckx%2FuBlock-Origin-filter%2Fmain%2Fdist%2Fgoogle%2Fglobal.txt&title=uBlock-Origin-filter%20-%20Google%20-%20Global)                  |                
| DuckDuckGo        |          [![uBO - add this filter](https://img.shields.io/static/v1?label=uBO&message=add%20this%20filter&color=fdd20a&style=flat&logo=uBlock%20Origin)](https://subscribe.adblockplus.org/?location=https%3A%2F%2Fraw.githubusercontent.com%2Femielderckx%2FuBlock-Origin-filter%2Fmain%2Fdist%2Fduckduckgo%2Fminecraft.txt&title=uBlock-Origin-filter%20-%20DuckDuckGo%20-%20Minecraft)           |
| Google+DDG        |      [![uBO - add this filter](https://img.shields.io/static/v1?label=uBO&message=add%20this%20filter&color=9b59b6&style=flat&logo=uBlock%20Origin)](https://subscribe.adblockplus.org/?location=https%3A%2F%2Fraw.githubusercontent.com%2Femielderckx%2FuBlock-Origin-filter%2Fmain%2Fdist%2Fgoogle_duckduckgo%2Fminecraft.txt&title=uBlock-Origin-filter%20-%20Google%2BDDG%20-%20Minecraft)      |
| Startpage         |           [![uBO - add this filter](https://img.shields.io/static/v1?label=uBO&message=add%20this%20filter&color=5b7bca&style=flat&logo=uBlock%20Origin)](https://subscribe.adblockplus.org/?location=https%3A%2F%2Fraw.githubusercontent.com%2Femielderckx%2FuBlock-Origin-filter%2Fmain%2Fdist%2Fstartpage%2Fminecraft.txt&title=uBlock-Origin-filter%20-%20Startpage%20-%20Minecraft)            |
| Brave             |               [![uBO - add this filter](https://img.shields.io/static/v1?label=uBO&message=add%20this%20filter&color=f25100&style=flat&logo=uBlock%20Origin)](https://subscribe.adblockplus.org/?location=https%3A%2F%2Fraw.githubusercontent.com%2Femielderckx%2FuBlock-Origin-filter%2Fmain%2Fdist%2Fbrave%2Fminecraft.txt&title=uBlock-Origin-filter%20-%20Brave%20-%20Minecraft)                |
| Ecosia            |              [![uBO - add this filter](https://img.shields.io/static/v1?label=uBO&message=add%20this%20filter&color=36acb8&style=flat&logo=uBlock%20Origin)](https://subscribe.adblockplus.org/?location=https%3A%2F%2Fraw.githubusercontent.com%2Femielderckx%2FuBlock-Origin-filter%2Fmain%2Fdist%2Fecosia%2Fminecraft.txt&title=uBlock-Origin-filter%20-%20Ecosia%20-%20Minecraft)               |
| All Search Engines | [![uBO - add this filter](https://img.shields.io/static/v1?label=uBO&message=add%20this%20filter&color=ffffff&style=flat&logo=uBlock%20Origin)](https://subscribe.adblockplus.org/?location=https%3A%2F%2Fraw.githubusercontent.com%2Femielderckx%2FuBlock-Origin-filter%2Fmain%2Fdist%2Fall_search_engines%2Fminecraft.txt&title=uBlock-Originfilter%20-%20All%20Search%20Engines%20-%20Minecraft) |


<details>
  <summary>How to import uBlock filters manually</summary>

### Manually import filters

  1. Open uBlock Origin settings
  2. Under the "Filter lists" tab, scroll to the bottom where it says “Custom” and click the “Import” checkbox to reveal the custom URL textbox
  3. Append the URL `https://raw.githubusercontent.com/emielderckx/uBlock-Origin-filter/main/dist/google_duckduckgo/all.txt` in the textbox
  4. Press `Apply Changes` in the upper left

  Note: In `dist/`, you can find filters for other search engines (Google, DuckDuckGo, Startpage or Brave). You can use and combine these filters by using the raw URL of `dist/` files.
</details>

<details>
  <summary>macOS Userscript</summary>

### macOS Userscript

For macOS users, this project also provide some Userscripts for Google+DuckDuckGo in `dist/userscript/google_duckduckgo/`

</details>

## Adding URL's

Please create a pull-request or [start an issue](https://github.com/emielderckx/uBlock-Origin-filter/issues/new?assignees=&labels=block-request&template=request-to-add-a-website-to-the-filter.md&title=Request%3A+add+COPYCAT_URL+to+the+filter) with evidence against the "copycats".

## Security

For simplicity and auto-updates, uBlock Origin filters rely on the last commit of the `main` branch, as every other uBO filters. For now, it seems this method does not raise security issues. However, you can import uBlock Origin filters with a reference to a given commit, not the `main` branch. Filters won't auto-update but they will be auditable by your own eyes.

## Scope of this filter

To me, a copycat is a website that:
- **mirrors most of GitHub/SO content**, automatically and without useful additional work on the content,
- **prevents** the user to **interact** easily with the resource (upvote, comment or reply),
- might **use SEO techniques** to catch users who would have otherwise reached the original resource,
- overall, **offers no benefits** for users over the original resource.

To be more precise:
- I do not consider automatic translation as a benefit;
- I do consider a mirror with clear attribution to be a copycat;
- I do not consider a mirror created for privacy concern to be a copycat, except if it uses aggressive SEO techniques;
- This uBlock filter is my own filter, for my usage and **can't obviously satisfy everyone**.

## Sources

* [Quenhus uBlock Origin dev filter](https://github.com/quenhus/uBlock-Origin-dev-filter)
* [Stop Mod Reposts Illegal Mod Sites](https://github.com/StopModReposts/Illegal-Mod-Sites)

## Do your own

1. List URL that you want to block in a `.txt` in the `data/` folder
2. Use `src/generate.py`, which generate files in `dist/` you can use as uBlock filters

Note: You can use [letsblock.it](https://letsblock.it/filters/search-results) to create your own filter.
