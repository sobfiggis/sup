# Sup

Sup is a console-based email client for people with a lot of email.

![Screenshot](/screenshot/split-horizontal.png?raw=true)

## [notmuch](https://notmuchmail.org/) integration

The `notmuch` branch is a WORKING-IN-PROGRESS to replace Sup's index backend with notmuch. It will reduce some features of Sup but would allow multiple Sup instances - Sup will be a "frontend" of notmuch.

Check the `forked` branch if you want to use Sup without notmuch.

## New features in this fork

- Basic mouse support.
- [Patchwork](http://jk.ozlabs.org/projects/patchwork/) integration. As the `.`, `o`, `x` in the screenshot, patch states can be easily observed.
- Async GUI editor support. You can edit multiple messages and browse other emails in Sup concurrently.
- Split view (experimental). By setting `:split_view` to `:vertical` or `:horizontal`, you can have more buffers in one screen.
- More flexible hooks. New hooks like `text-filter`, `collapsed-header` make things more flexible.
- Various fixes and improvements. For example, respect editor's exit code, no more "bundle exec", better cygwin support, etc. Read commit log for details.

## Installation

[See the wiki][Installation]

## Features / Problems

Features:

* GMail-like thread-centered archiving, tagging and muting
* [Handling mail from multiple mbox and Maildir sources][sources]
* Blazing fast full-text search with a [rich query language][search]
* Multiple accounts - pick the right one when sending mail
* [Ruby-programmable hooks][hooks]
* Automatically tracking recent contacts

Current limitations:

* Sup does in general not play nicely with other mail clients, not all
  changes can be synced back to the mail source. Refer to [Maildir Syncback][maildir-syncback]
  in the wiki for this recently included feature. Maildir Syncback
  allows you to sync back flag changes in messages and to write messages
  to maildir sources.

* Unix-centrism in MIME attachment handling and in sendmail invocation.

## Problems

Please report bugs to the [Github issue tracker](https://github.com/sup-heliotrope/sup/issues).

## Links

* [Homepage](http://sup-heliotrope.github.io/)
* [Code repository](https://github.com/sup-heliotrope/sup)
* [Wiki](https://github.com/sup-heliotrope/sup/wiki)
* IRC: [#sup @ freenode.net](http://webchat.freenode.net/?channels=#sup)
* Mailing list: supmua@googlegroups.com (subscribe: supmua+subscribe@googlegroups.com, archive: https://groups.google.com/d/forum/supmua )

## License

```
Copyright (c) 2013       Sup developers.
Copyright (c) 2006--2009 William Morgan.

This program is free software; you can redistribute it and/or
modify it under the terms of the GNU General Public License
as published by the Free Software Foundation; either version 2
of the License, or (at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program; if not, write to the Free Software
Foundation, Inc., 51 Franklin Street, Fifth Floor, Boston, MA
02110-1301, USA.
```

[sources]: https://github.com/sup-heliotrope/sup/wiki/Adding-sources
[hooks]: https://github.com/sup-heliotrope/sup/wiki/Hooks
[search]: https://github.com/sup-heliotrope/sup/wiki/Searching-your-mail
[Installation]: https://github.com/sup-heliotrope/sup/wiki#installation
[ruby20]: https://github.com/sup-heliotrope/sup/wiki/Development#sup-014
[maildir-syncback]: https://github.com/sup-heliotrope/sup/wiki/Using-sup-with-other-clients
