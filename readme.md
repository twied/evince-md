evince-md
=========

What's this?
------------

I wish Gnome's Evince could present Markdown. There is a pretty old
[feature request](https://gitlab.gnome.org/GNOME/evince/-/issues/388) though.

This is a simple wrapper around pandoc to turn Markdown files into PDF. It
keeps the PDF in sync with the Markdown file as long as Evince is open, i.e.
if you edit and save your Markdown file, Evince will pick up the changes.

Options
-------

If you have options (or "metadata" in pandoc) that you want to have applied,
put them in `${HOME}/.config/evince-md/metadata.yml`. Mine looks like this:

```.yml
---
numbersections: true
colorlinks: true
...
```

Installation
------------

Put the script somewhere suitable, e.g. `${HOME}/bin` or `${HOME}/.local/bin`,
and change your default file association for markdown files to have them opened
with this script.

License
-------

I believe that this script barely qualifies as worth putting a license on, but
in the spirit of open source, all files in this repository are placed under the
GNU General Public License version 2 or later ("GPL v2+").

Resources
---------

* Evince: https://wiki.gnome.org/Apps/Evince
* Pandoc: https://pandoc.org/
* Values to put in your `metadata.yml`: https://pandoc.org/MANUAL.html#variables-for-latex
* A Google Chrome plugin that renders Markdown beautyfully but breaks more and
  more with every Chrome update: https://chrome.google.com/webstore/detail/markdown-reader/gpoigdifkoadgajcincpilkjmejcaanc
