cloc2json
=========

A simple package to convert CLOC CSV output into JSON.

# Usage

If you want the lines of code in a given code base, 
you can use the handy [cloc](http://cloc.sourceforge.net/) tool that is widely available.

It generates an overview of the programming languages, files and the number of lines of code in each file (or the whole project).

To be able to use this output programmatically, you can use cloc2json to turn it into JSON for further processing or digestion:

```shell
  $ npm install -g cloc2json
  $ cloc --by-file --report-file output.cloc --csv path/to/code
  $ cloc2json output.cloc > output.json
```

# License

This project is MIT licensed.
