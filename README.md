# [elomatreb.eu](https://elomatreb.eu)

![Build status](https://api.travis-ci.org/elomatreb/website.svg?branch=master)

My personal website, blog and portfolio. Built using [Jekyll][jekyll].

## Development

Once you have cloned the repository, execute `bundle install` to get all 
necessary gems.

Since the SCSS utilizes [Bourbon](https://github.com/thoughtbot/bourbon), it is 
necessary to install the files manually.

```
$ bourbon install --path=css/
```

The `Rakefile` in this repository provides several commands useful if you want 
to build a local copy of the site.

## Legal

This project uses a modified version of the [code snippet plugin of Octopress](https://github.com/imathis/octopress), 
which is released under the MIT License.

All files inside the `_posts/` directory are released under the terms of the 
[Creative Commons Attribution 4.0 International](https://creativecommons.org/licenses/by/4.0/)
license.

All other files are released under the MIT License (See [LICENSE.md](LICENSE.md) for details).
