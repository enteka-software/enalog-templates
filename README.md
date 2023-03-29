# EnaLog Templates

This repository contains a number of templates showing examples of how EnaLog can be used for so much more than just event tracking

### Waitlists

EnaLog can be used for building a waitlist for your startup. We have created a number of free templates which show how this can be done

* [waitlist-astro](/waitlist-astro/) - built with Astro

### How to clone a single template

Whilst cloning a single template is possible using a `spare-checkout` it can be rather complex. Instead I'm going to show you how to clone the repo and use a single template as a new git repo

1. Clone the whole repo:
```
git clone git@github.com:enteka-software/enalog-templates.git
```
2. Make a directory to copy your chosen template to: `mkdir /path/to/new/dir`
3. Copy the chosen template to your new created directory: 
```
cp -r enalog-templates/<chosen-template> /path/to/new/dir
```
4. Inside your new directory initialise a git repo with `git init`