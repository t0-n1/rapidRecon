# rapidRecon

## Usage

There are three modes of operation:

### download

Download the latest DNS record file (default: cname) from [Rapid 7 Open Data](https://opendata.rapid7.com/).

```
$ ./rapidRecon download
$ ./rapidRecon download [a|aaaa|any|caa|cname|mx|ns|txt]
```

### list

List all available providers. Each provider contains a list of subdomains that can also be listed, which are used in the search mode to filter the DNS record file.

```
$ ./rapidRecon list
$ ./rapidRecon list [provider]
```

### search

Search for a pattern in the DNS record file. Three submodes of operation:
- all: iterate all providers and for each one filter by provider subdomains before searching for the pattern.
- &lt;provider&gt;: filter by provider subdomains before searching for the pattern.
- open: search directly for the pattern.

Set COLOR=true to highlight the filter and pattern results.

```
$ [COLOR=true] ./rapidRecon search all <pattern> <file>
$ [COLOR=true] ./rapidRecon search <provider> <pattern> <file>
$ [COLOR=true] ./rapidRecon search open <pattern> <file>
```
