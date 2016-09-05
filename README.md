# Welcome to my Website

## Introduction

This repository is for the website <http://ankitkamboj.com>

## Adding Blog Posts:

New blog posts can be created by adding a new markdown file in \_posts directory in format 'yyyy-mm-dd-name-of-file.md'
This will publish the blog to the website.

## Updating profile information

    + Go to \_config.yml, and update the required information.

## Adding Training Content

To add new training content add to one of the provided modules:
  + train-framework
    - add table of content file at \_train-framework collection folder.
    - note that this module is geared towards application framework and libraries

  + train-language
    - add table of content file at \_train-language collection folder.
    - note that this module is geared towards programming languages.

  + train-tdd
    - add table of content file at \_train-tdd collection folder.
    - note that this module is geared towards Test Driven Development approach, notably for unit testing and integration testing tutorials

  + train-tools
    - add table of content file at \_train-tools collection folder.
    - note that this module is geared towards build and productivity tools

## Adding Tutorial Series

To add new tutorial series, follow the following process.

  + Add collection folder
    - add a new folder to root, in format '\_tut-<name>'
    - this folder will contain all tutorials in a tutorial series.
    - try to prefix the tutorial lesson files with numerics for easy organisation.

  + Add configuration to '\_config.yml'
    - under collection configurations, add the reference for the new collection folder & its required configurations.
    - under defaults, define the default values for the new tutorial series collection.

  + Add tutorial nav list
    - add navigation sidebar to tutorial series, in '\_data/navigation.yml' file.

  + Display on Tutorial page
    - to display a newly created tutorial series on tutorials page, add the following code to the page end, and replace 'tut-<name>' with actual collection name.

      ```jekyll
      <div class="grid__wrapper">
        {% for post in site.tut-<name> limit:1%}
          {% include archive-single.html type="grid" %}
        {% endfor %}
      </div>

      {% include feature_row id="end" type="center"%}
      ```

## Updating CSS class
    To update the CSS, update the required .sass file and then generate the main.css using the below script

    ```
      npm run build:css
    ```

## Building & Serving website
    To build and fire a local jekyll website use the below script.

    ```
      sudo bundle exec jekyll serve
    ```

    > Note: updates to '\_config.yml' requires restarting the server

---
###### Thanks to **Minimal Mistakes**, an awesome jekyll based theme.

###### The MIT License (MIT)

###### Copyright (c) 2016 Michael Rose

###### Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

###### The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

###### THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
