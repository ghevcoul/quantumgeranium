# quantumgeranium
Content and scripts used for making quantumgeranium.com

## Theme
Site uses the public domain [blue-penguin](https://github.com/jody-frankowski/blue-penguin). 

## Steps to generate the site and deploy
The HTML content is built using the [Pelican](https://blog.getpelican.com/) static site generator.
Once the content is built, it is committed to the `gh-pages` branch using the [ghp-import](https://github.com/davisp/ghp-import) tool.

```shell script
$ pelican content -o output -s pelicanconf.py
$ ghp-import output -b gh-pages
$ git push origin gh-pages
```