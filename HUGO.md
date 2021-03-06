# HUGO Tutorial




## General

[What is a Static Site Generator? And 3 ways to find the best one](https://www.netlify.com/blog/2020/04/14/what-is-a-static-site-generator-and-3-ways-to-find-the-best-one/)

## Getting Started

[Whole Tutorial](https://www.youtube.com/playlist?list=PLLAZ4kZ9dFpOnyRlyS-liKL5ReHDcj4G3)

2. [Installing Hugo on Windows](https://www.youtube.com/watch?v=G7umPCU-8xc)

3. [Installing Hugo on Mac](https://www.youtube.com/watch?v=WvhCGlLcrF8)

4. [Creating a New Site / Directory Structure](https://www.youtube.com/watch?v=sB0HLHjgQ7E)

5. [Installing & Using Themes](https://www.youtube.com/watch?v=L34JL_3Jkyc)

## Hugo Commands

```
> hugo help
hugo is the main command, used to build your Hugo site.

Hugo is a Fast and Flexible Static Site Generator
built with love by spf13 and friends in Go.

Complete documentation is available at http://gohugo.io/.

Usage:
  hugo [flags]
  hugo [command]

Available Commands:
  config      Print the site configuration
  convert     Convert your content to different formats
  deploy      Deploy your site to a Cloud provider.
  env         Print Hugo version and environment info
  gen         A collection of several useful generators.
  help        Help about any command
  import      Import your site from others.
  list        Listing out various types of content
  mod         Various Hugo Modules helpers.
  new         Create new content for your site
  server      A high performance webserver
  version     Print the version number of Hugo

Flags:
  -b, --baseURL string         hostname (and path) to the root, e.g. http://spf13.com/
  -D, --buildDrafts            include content marked as draft
  -E, --buildExpired           include expired content
  -F, --buildFuture            include content with publishdate in the future
      --cacheDir string        filesystem path to cache directory. Defaults: $TMPDIR/hugo_cache/
      --cleanDestinationDir    remove files from destination not found in static directories
      --config string          config file (default is path/config.yaml|json|toml)
      --configDir string       config dir (default "config")
  -c, --contentDir string      filesystem path to content directory
      --debug                  debug output
  -d, --destination string     filesystem path to write files to
      --disableKinds strings   disable different kind of pages (home, RSS etc.)
      --enableGitInfo          add Git revision, date and author info to the pages
  -e, --environment string     build environment
      --forceSyncStatic        copy all files when static is changed.
      --gc                     enable to run some cleanup tasks (remove unused cache files) after the build
  -h, --help                   help for hugo
      --i18n-warnings          print missing translations
      --ignoreCache            ignores the cache directory
      --ignoreVendor           ignores any _vendor directory
  -l, --layoutDir string       filesystem path to layout directory
      --log                    enable Logging
      --logFile string         log File path (if set, logging enabled automatically)
      --minify                 minify any supported output format (HTML, XML etc.)
      --noChmod                don't sync permission mode of files
      --noTimes                don't sync modification time of files
      --path-warnings          print warnings on duplicate target paths etc.
      --print-mem              print memory usage to screen at intervals
      --quiet                  build in quiet mode
      --renderToMemory         render to memory (only useful for benchmark testing)
  -s, --source string          filesystem path to read files relative from
      --templateMetrics        display metrics about template executions
      --templateMetricsHints   calculate some improvement hints when combined with --templateMetrics
  -t, --theme strings          themes to use (located in /themes/THEMENAME/)
      --themesDir string       filesystem path to themes directory
      --trace file             write trace to file (not useful in general)
  -v, --verbose                verbose output
      --verboseLog             verbose logging
  -w, --watch                  watch filesystem for changes and recreate as needed

Additional help topics:
  hugo check   Contains some verification checks

Use "hugo [command] --help" for more information about a command.
```
### Create New Site

Creates a new site with its folder structure in the current directory.

> hugo new site [site-name]

Don't use blank spaces in the site's name, use underscore or dash instead.

## Folder Structure

**archetypes**

Contains markdown files named after content types on your site. Examples of this would be: blog.md, work.md, and of course, pizza.md. Inside these "archetypes" are default parameters defined via front matter that every new piece of content associated with this archetype will inherit. When you first start a new Hugo project the archetypes/ directory will only contain a default.md file. All new content files generated via the command line will inherit from this archetype unless an archetype exists specifically for that content type.

**content**

Holds all the content of your site.

It is made up of the sections and static pages that structure a website. There's a distinct difference between the terms sections and static pages and it's pretty easy to grasp:

A *section* is a portion of the site that holds subcontent, such as a blog section and a work section. The blog section contains individual blog posts, and the work section is a portfolio of individual projects.

A *static page* is simply a page that renders content and nothing else. It doesn't need to index a list of subcontent for the user to peruse. The about page is a good example. If you view it in the browser, you can't go down any further. It's the about page and that's it.

The _index.md file plays an important role here. Hugo requires that an _index.md file be explicity defined at the root of content/, and it uses this file to render the homepage of your site.

**data**

Contains data in e.g. JSON files that can be used to build the site. It serves as a replacement to a database.

**layouts**

A directory of templates. Each provides a consistent layout when rendering the markdown files that exist in content/. Can contain files like *header.html* and *footer.html* that will be similar across the whole site.

**static**

All assets are placed here and can then be used throughout the project. Images, css, js files...

**themes**

For 3rd party themes.

**config.toml**

Config for the whole site.

https://github.com/JulienD/Hugo-Cheatsheet

https://www.jakewiesler.com/blog/hugo-directory-structure

https://jpdroege.com/blog/hugo-file-organization/
