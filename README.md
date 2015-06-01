ated4kids website
=================

How to modify the site
---------------

The website has been built using [middleman](http://middlemanapp.com/)

* the base layout for all the pages (currently only the main page) is `source/layouts/main.erb`
* all the multi-language pages must be placed into the `source/localizable/` folder
* all the template fragments must be placed into the `source/partials/` folder and must follow middleman's naming conventions
* all the yaml language files must be placed into the `locales/` folder

How to add a blog post
---------------
in the blog/blarticles directory create a new .html.markdown file (or start from one of the existing files) and write the content using standard HTML
Page links and indexes will be automatically generated by middleman during build.

Note: Blog post must have a date that is in the past (when building) otherwise they will not appear on the website

How to add an event page
---------------
in the events/evarticles directory create a new .html.markdown file (or start from one of the existing files) and write the content using standard HTML
Page links and indexes will be automatically generated by middleman during build.

Note: Events pages must have a date that is in the past (when building) otherwise they will not appear on the website

How to run locally
------------------
```
$ bundle exec middleman server
```

How to publish the site on github pages
------------------
Option 1: 
Publish you local repo directly on ated4kids.ch:
```                   
rake publish
```

if you have uncommitted code in you local repo use:
```                   
rake publish ALLOW_DIRTY=true
```

Option 2: 

Commit and push your changes on master branch
```                   
$ git commit -m "DESCRIPTION_OF_CHANGE"
$ git push origin
```

Note: if you don't have permissions to push on ated4kids repository, please submit a Pull Request (PR)

The master branch will then be built from codeship.io and deployed on gh-pages branch

[ ![Codeship Status for ated4kids/website](https://codeship.com/projects/fbb84de0-23f5-0132-4e4e-7e9ae55fd39f/status?branch=master)](https://codeship.com/projects/36762)
