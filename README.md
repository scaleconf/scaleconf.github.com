ScaleConf website
=================

This repository contains the jekyll code to generate the scaleconf.org website.

Pull-requests are welcome if you spot any problems as the conference gets organised.

## How to dev:

### Generic

Install dependencies:
```
bundle install
```

Run a local server:
```
bundle exec jekyll server
```

Point your web browser at `http://127.0.0.1:4000/`, any time you save a file the server will reload and you can browse the changes in your browser.

### Docker

There is a generic github-pages dockerfile we can just use

```
docker run -v "$PWD":/usr/src/app -p "4000:4000" starefossen/github-pages
```

You can then point your browser at your docker instance, on mac this is probably docker-machine, so something like `http://192.168.99.100:4000/`

## Images

### Sponsors

Sponsors should be padding in such a way that the text is roughly consistent
in sizing. This isn't an exact science unfortunately, and just needs to be looked
at in the context of other sponsors logo's to ensure that some aren't super small
because of the way their logo spacing works.

To resize, I found it mostly easiest to just use image magick.

to take a tightly cropped logo and add some padding, and resize it to 50% of the size

```bash
convert logo.png -gravity center -background white -extent 130x130% -resize 50% logo.large.png
```
