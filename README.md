**THIS FUNCTIONALITY HAS BEEN MOVED TO https://github.com/tdegeus/GooseBib. In time this respository will be removed**

# bibparse

Parse a BibTeX file to a cleaner version in which only the relevant fields are stored. Also, the names of authors are uniformly stored.

```bash
# Basic usage
bibparse INPUT.BIB [OUTPUT.BIB]

# Getting help
bibparse --help
```

## Options

*   `--duplicate-authors`

    Check if the same authors are stored differently in the input BibTeX file. `bibparse` will check which authors are converted to the same 'cleaned' author name. This option does not influence the result, but does provide information to manage the input BibTeX file.

*   `--check-keys`

    Check citation keys for first author + year construction. The keys that are not matching this construction are printed to the screen (excluding `@misc` entries). This option does not influence the result, but does provide information to manage the input BibTeX file.

*   `--author-sep STR`

    Set character to separate authors' initials. By default, the initials are
    not separated. For example, the default `T.W.J.\` can converted to
    `T.~W.~.J.\` using `--author-sep="~"`.

## Dependencies

`bibparse` depends on Python3 and its `bibtexparser` module. Install this Python3 module using: 

```bash
pip3 install bibtexparser
```
