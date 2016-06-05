# Parsedown filter

Provides basic and optionaly extra markdown filter integration for Backdrop input formats. 
Filter based on http://parsedown.org markdown parser with Markdown Extra support.

**Important note about running Markdown with other input filters**

Parsedown filter may conflict with other input filters, depending on the order
in which filters are configured to apply. If using Parsedown Filter produces
unexpected markup when configured with other filters, experimenting with
the order of those filters will likely resolve the issue.

The "Limit allowed HTML tags" filter is a special case:

For best security, ensure that it is run after the Markdown Extra filter
and that only markup you would like to allow in via HTML and/or Markdown
Extra is configured to be allowed via the it.

If you on the other hand want to make sure that all converted Markdown
text is preserved, run it after the Markdown Extra filter. Note that
blockquoting with Parsedown Filter doesn't work when run after "Limit allowed
HTML tags". It converts the ">".

##Installation
- Install this theme using the official Backdrop CMS instructions at https://backdropcms.org/guide/themes

##Current Maintainer
- Gor Martsen (http://github.com/Gormartsen)

##Credits
- [prasedown](https://github.com/erusev/parsedown) that do Markdown processing created by [Emanuil Rusev](https://github.com/erusev)


##License

The Backdrop module code is GPL v2 software, but the Parsedown library is distributed under separate licence MIT.
See more details on library page (https://github.com/erusev/parsedown)
