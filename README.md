# Source Deps Reviewer

## Synopsis

This is a tool for labeling dependencies with a web interface.

Basically, it greps the specified directory for the given pattern,
and let human reviewers label their dependencies, even code dependencies,
which are code segments that are highly related to the specific pattern.

## Installation and Dependencies

This tool depends on [codesearch](https://github.com/google/codesearch)
to generate regular expression index, please install them with:

```
$ go get github.com/google/codesearch/cmd/cindex
$ go get github.com/google/codesearch/cmd/csearch
```

Note that the index file locates at ~/.csearchindex by default.

This tool depends on several Python packages,

```
$ pip install -e .
```

To run functional test, please do

```
$ pip install -e .[dev]
```

Prism, a code syntax highlighter is used.
It can be found at https://github.com/PrismJS/prism

## Usage

```
$ sourcedr --android-root DIRECTORY_ROOT_PATH --pattern PATTERN_TO_GREP
```

Add flag --is-regex if the pattern given is a regex open browser at
[localhost:5000](localhost:5000)

You can customize settings by editing `config.py`

## Testing

```
$ python3 functional_tests.py
```
