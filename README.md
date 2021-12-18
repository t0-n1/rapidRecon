# rapidRecon

## Usage

There are three modes of operation:

### download

Download the latest CNAMEs file from [Rapid 7 Open Data](https://opendata.rapid7.com/).

```
$ ./rapidRecon download
```

### list

List all available providers. Each provider contains a list of subdomains that are used in the search mode to filter the CNAMEs file, which can also be listed.

```
$ ./rapidRecon list
$ ./rapidRecon list [provider]
```

### search

Search for a pattern in the CNAMEs file.
Three submodes of operation:
- all: iterate all providers and for each one filter by provider subdomains before searching for the pattern.
- "provider": filter by provider subdomains before searching for the pattern.
- open: search directly for the pattern.

```
$ ./rapidRecon search all <pattern> <file>
$ ./rapidRecon search <provider> <pattern> <file>
$ ./rapidRecon search open <pattern> <file>
```
