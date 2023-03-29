> my resume

# Usage

Easiest way to compile to `pdf` is to use [docker-texlive docker image](https://github.com/thomasWeise/docker-texlive)

The command to build the resume is `make pdf`

To automatically update the git version run `make build` which requires a clean git repository to succeed.

```
docker run -it \
    -v `pwd`/static/cv:/doc/ \
    -v `pwd`/static/cv/fonts/:/usr/share/fonts/external \
    -v `pwd`/patch/__texSetup__.sh:/patch/__texSetup__.sh \
    thomasweise/texlive \
    cp /patch/__texSetup__.sh /usr/bin/__texSetup__.sh && xelatex.sh cv-lihs.tex
```

# Attributions

* uses [friggeri cv](http://www.latextemplates.com/template/friggeri-resume-cv) as base
* fonts inspired by [deedy-resume](https://github.com/deedy/Deedy-Resume)
* some custom modifications

# License

[CC BY-SA 4.0](LICENSE)
