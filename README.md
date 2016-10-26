# contextual-search

This plugin replaces the default [search](https://github.com/GitbookIO/plugin-search) plugin for GitBook, it adds some contextual sorting to the search results.

This plugin uses the [lunr-depth](https://github.com/jrwells/gitbook-plugin-lunr-depth) backend.

### Usuage

The default [search](https://github.com/GitbookIO/plugin-search) must be disabled using a book.json configuration and this plugin must be added:

```
{
    plugins: ["-search", "contextual-search"]
}
```

## search

This is *mostly* a drop in replacement for the default [search](https://github.com/GitbookIO/plugin-search) plugin, most of the original functionality is still present;
the backend is slightly less agnostic because it relies on depth information.


#### Adding keywords to a page

You can specify explicit keywords for any page. When searching for these keywords, the page will should rank higher in the results.

```md
---
search:
    keywords: ['keyword1', 'keyword2', 'etc.']
---

# My Page

This page should be among the first search results for "keyword1".
```

#### Disabling indexing of a page

You can disable the indexing of a specific page by adding a YAML header to the page:

```md
---
search: false
---

# My Page

This page should not appear in the search results.
```
