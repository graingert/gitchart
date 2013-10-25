## Description

`gitchart.py` is a Python script to build charts from a Git repository.

It can build following charts, as SVG or PNG:

* authors (pie chart)
* commits by hour, day of week, month of year, year, year/month (bar charts)
* commits by hour of week (dot chart)
* files by type (pie chart)

## Install

The script requires Python >= 2.7 and [Pygal](http://pygal.org/), which can be
installed with this command:

    # pip install pygal

Note: cairosvg is required to generate PNG files.

## Examples

Generate pie chart with authors:

    $ python gitchart.py authors "Git authors" /path/to/gitrepo/ authors.svg

Generate bar chart with commits by year:

    $ python gitchart.py commits_year "Git commits by year" /path/to/gitrepo/ commits_year.svg

Generate bar chart with commits by version (tag):

    $ cd /path/to/gitrepo/
    $ git tag | python /path/to/gitchart.py commits_version "Git commits by version" . /tmp/commits_version.svg

## Demo

`gitchart.py` is used to build statistics for WeeChat: http://weechat.org/dev/stats/
