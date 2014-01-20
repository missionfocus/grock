# grock

[Grock](http://killercup.github.io/grock/) converts your nicely commented code into a gorgeous documentation where comments and code live happily next to each other.

To see how it works, just have a look at [the documentation rendered from this repository](http://killercup.github.io/grock/).

## Inspiration

- [Literate programming](http://en.wikipedia.org/wiki/Literate_programming) (the programming methodology coined by [Donald Knuth](http://en.wikipedia.org/wiki/Donald_Knuth))
- [Jeremy Ashkenas](https://github.com/jashkenas)' [docco]
- The [groc] project -- this implementation is heavily based on this, but uses node.js streams
- [Gulp.js](http://gulpjs.com/), a build system that uses streams to transform files

### What makes grock different?

In contrast to other node-based documentation generators like [docco], [docker], and [groc], groc has the following advantages:

- It doesn't need pygments.
- Therefore it doesn't need python.
- Therefore it's faster than those other tools that need pygments.
- It renders a file tree and also a headline tree for each document.
- The default style (based on solarized) is responsive and looks actually quite good on a phone.
- It's based on streams. I've heard all the cool kids are using streams now.

[docco]: http://jashkenas.github.com/docco/
[docker]: https://github.com/jbt/docker
[groc]: http://nevir.github.com/groc/

## Based on

- [vinyl-fs](https://github.com/wearefractal/vinyl-fs) for abstracting files
- [Solarized](http://ethanschoonover.com/solarized)
- [marked](https://github.com/chjj/marked)
- [highlight.js](http://highlightjs.org/)

Oh, and all the heavy lifting (splitting code and comments, parsing doc tags) is actually code from [groc](http://nevir.github.com/groc/)!

## Roadmap

- [x] Be awesome with streams
- [x] Split code and comments
- [x] Highlight code
- [x] Generate TOC as JSON file
- [x] Render doc tags (like jsdoc)
- [x] CLI docs, `.groc.json` config support
- [ ] Correctly parse relative roots
- [ ] Tests. Test for everything.
- [ ] Add another style.
- [ ] Find a streaming code highlighter with hooks for comment segments
