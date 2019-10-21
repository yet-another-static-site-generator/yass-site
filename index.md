-- All lines which starts with double minus sign are comments and ignored by program. Unless they have colon sign. Then they are tags definition.
-- Ada Web Server template which will be used as HTML template for this file. Required for each file
-- layout: default
-- You may add as many tags as you want and they can be in any place in file, not only at beginning. Tags can be 4 types: strings, boolean, numeric or composite.
-- First 3 types of tags are in Name: Value scheme. For strings it can be any alphanumeric value without new line sign. For boolean it must be "true" or "false", for numeric any number. Program will detect self which type of tag is and properly set it. It always fall back to string value.
-- Composite tags first must be initialized with Name: [] then just add as many as you want values to it by Name: Value scheme.
-- For more informations about tags please check program documentation.
-- If you have enabled creation of sitemap in the project config file, you can set some sitemap parameters too. They are defined in this same way like tags, with ParameterName: Value.
-- priority - The priority of this URL relative to other URLs on your site, value between 0.0 and 1.0.
-- changefreq - How frequently the page is likely to change, value can be always, hourly, daily, weekly, monthly, yearly or never.
-- For more informations how this options works, please look at the program documentation.
-- Additionally, you can exclude this file from adding to sitemap by setting option insitemap: false.
-- If you have enabled creating Atom feed for the site, you must specify "title" tag for this page. If you will use this file as a main source of Atom feed, then you must add "title" tag for each section which will be used as source for Atom feed entry. If you want to set author name for Atom feed, you must add "author" tag. If you want to set author email for Atom feed, you must add "authoremail" tag. If you want to add short entry summary, you must add tag "summary". Did that tags will be for whole page or for each entry depends on your Atom feed configuration.
-- title: Yet Another Static Site (Generator)
-- You can without problem delete all this comments from this file.

As name says, it is static site generator written in Ada. It is
*headless* application (no user interface, use it from console). Main
goal of the project is create simple static site generator, with some
basic functions but easily extendable. The program is available only
for Linux 64-bit. For more informations about the program, please
look at [documentation](docs/user/index.html).

<div id="center"><a class="button" href="docs/user/quickstart.html">Quick start</a></div>

## Features

-   Advanced [Ada Web Server HTML templates](http://docs.adacore.com/aws-docs/templates_parser/)

    Composite tags allows easily creating lists or tables without HTML
    inside markdown files. Including system allow split and merge sites
    layouts on few reusable elements.

-   Full CommonMark support via
    [libcmark](https://github.com/commonmark/cmark)

    Everything what is possible in [CommonMark](https://commonmark.org/)
    will be parsed to HTML.

-   Support almost infinite amount of custom tags in HTML templates
    (depends on available RAM) and separated tags for whole site and
    each page

    Just add [tags](docs/tags.html) to the site project configuration
    file or directly to markdown files.

-   Fast

    Just Ada and C. Should be one of the fastest static site generator
    available.

-   Can be extended with modules, written in any script/programming
    language

    Anything what can be run on your computer/server can be used as the
    program [module](docs/user/extending.html).

-   Can generate [sitemaps](https://www.sitemaps.org/)

    Generate sitemaps for the search engines, fully configurable. Can be
    disabled.

-   Can generate [Atom feeds](https://validator.w3.org/feed/docs/atom.html)

    Generate simple Atom feeds from pages or choice one page as a source
    for the feed. Can be disables either.

-   Auto reconfigure server when configuration file was changed

    The program in server mode monitor the site configuration file
    periodically and reconfigure self if needed. You don\'t need to stop
    it and restart to apply configuration changes.

## Links

-   Last release:
    [1.0](https://github.com/yet-another-static-site-generator/yass/releases/tag/v1.0)
    (2019-03-25)
-   [Latest release documentation](docs/user/index.html)
-   [GitHub](https://github.com/yet-another-static-site-generator/yass)

## Donate

If you want to support the program development, you can donate some
money by Liberapay or Patreon.

<a href="https://liberapay.com/thindil" class="image"><img alt="Donate using Liberapay" src="https://liberapay.com/assets/widgets/donate.svg"></a> <a href="https://www.patreon.com/thindil" class="image"><img alt="Become a Patron!" src="assets/images/patreon.png" width="150"></a>
