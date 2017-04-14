# bibparse

Parse a bib-file to a cleaner version in which only the fields that are relevant to BibTeX are stored, and the names of authors are uniformly stored.

## Dependencies

`bibparse` depends on `bibtexparser`. Install this Python module using: 

```bash
pip install bibtexparse
```

## Usage

```bash
# Basic usage
bibparse INPUT.BIB [OUTPUT.BIB]

# Getting help
bibparse --help
```

## Options

*   `--duplicate-authors`

    Check if the same authors are stored differently in the input bib-file. `bibparse` will check which authors are converted to the same "cleaned" author name. This option therefore does not influence the result, but does provide information to manage the input bib-file.

*   `--author-sep STR`

    Set character to separate authors' initials. By default, the initials are
    not separated. For example, the default `T.W.J.\` can converted to
    `T.~W.~.J.\` using `--author-sep="~"`.

*   `--check-keys`

    Check citation keys for first author + year construction.
