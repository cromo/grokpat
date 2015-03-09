# grokpat

Call up grok patterns for use in command line programs.

## Overview

[Grok](http://logstash.net/docs/1.4.2/filters/grok) is a system for composable, named regular expressions. It is a common processing step in the [Logstash](http://logstash.net/) portion of the ELK stack. Due to its popularity, there are a number of community maintained grok patterns for many formats that have been battle tested as correct, but they are stuck in grok's pattern format language. Grokpat can take names of grok patterns and prints out the fully expanded regular expression that corresponds to it, allowing use of these known-working patterns outside of grok.

## Installation

Put `grokpat` on your path. If you would like it to load some patterns by default, it looks for files or directories named `$script_dir/grok-patterns` and `$HOME/.grok-patterns`. A good set of sample patterns come from the [logstash patterns directory](https://github.com/elasticsearch/logstash/tree/v1.4.2/patterns).

## Usage

```
grokpat [--raw] (--pattern-file=<file_or_dir>|<pattern_name>)...
```

Where pattern names are the case-insensitive names of the patterns in the grok files.

`--raw` prevents the pattern from being expanded, instead returning the pattern using grok syntax.

`--pattern-file=...` Adds another file or directory to the list of patterns to draw from. Directories are loaded non-recursively in alphabetical order.

## License

Grokpat is licensed under the MIT license. The full license is in the `LICENSE` file.
