nbcount is a naive, bad counter for source code.

Currently only supports code with single line comment starting with one of:

- `#`
- `"`
- `%`
- `--`
- `//`
- `REM`

No support for multi-line comments.
No distinguish comment marks between languages,
for example, `REM = 2` in C will be considered as comment line (not count).


Install
--------

### Dependencies

- sh
- grep
- wc

### With `make`

```sh
; git clone https://github.com/weakish/nbcount
; cd nbcount
; make
```

Files will be installed to `/usr/local/bin`.
If you want to install other place, edit `config.mk` before running `make`.

Makefile is compatible with both GNU make and BSD make.

### With basher

```sh
; basher install weakish/nbcount
```

### Manually

Copy `bin/nbcount` to `$PATH`.

Usage
------

    cat source.code | nbcount

License
--------

0BSD
