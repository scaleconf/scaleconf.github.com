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

You can then point your browser at your docker instance, on mac this is probably docker-machine, so something like `http://http://192.168.99.100:4000/`
