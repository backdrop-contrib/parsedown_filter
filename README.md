# Parsedown filter

Provides basic and optionally extra markdown filter integration for Backdrop
input formats. Filter based on [Parsedown](https://parsedown.org) markdown parser with
Markdown Extra support.

**Important note about running Parsedown filter with other input filters**

Parsedown filter may conflict with other input filters, depending on the order
in which filters are configured to apply. If using Parsedown filter produces
unexpected markup when configured with other filters, experimenting with the
the order of those filters will likely resolve the issue.

The "Limit allowed HTML tags" filter is a special case:

For best security, ensure that it is run after the Markdown Extra filter and
that only markup you would like to allow in via HTML and/or Markdown Extra is
configured to be allowed by it.

If you, on the other hand, want to make sure that all converted Markdown text
is preserved, run it after the Markdown Extra filter. Note that
blockquoting with Parsedown filter doesn't work when run after "Limit allowed
HTML tags". It converts the ">".

## Installation

- Install this module using the official Backdrop CMS instructions at
https://backdropcms.org/guide/modules

## Current Maintainer

- [Martin Price](https://github.com/yorkshire-pudding) -
[System Horizons Ltd](https://www.systemhorizons.co.uk)

## Credits

- Created for Backdrop CMS by [Gor Martsen](http://github.com/Gormartsen)
- [Parsedown](https://github.com/erusev/parsedown) created by
[Emanuil Rusev](https://github.com/erusev)

## License

The Backdrop module code is GPL v2 software, but the Parsedown and Parsedown
Extra libraries are distributed under separate licence (MIT). See more details
on the library pages for [Parsedown](https://github.com/erusev/parsedown) and
[Parsedown Extra](https://github.com/erusev/parsedown-extra).