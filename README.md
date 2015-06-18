# WAV → FLAC and/or MP3

This script can convert `.wav` files into FLAC or MP3 format using `flac` or
`lame` encoders respectively. It's created to produce properly tagged, high
quality versions of «master» files. Main features:

* when file name has numeric prefix it parses it and writes it as «tract
  number» tag;

* it can also automatically write «track title» tag;

* it can automatically count total number of supplied files and write this
  number as «total tracks» tag;

* it accepts various options like «album artist» and «album title» and
  passes them to corresponding encoder, this way you don't need to remember
  different options for every encoder (`flac` or `lame`), `wav2` gives you
  level of abstraction;

* it can accept many files at once;

* it can convert to both FLAC and MP3 formats via one invocation;

* output directory can be specified (and created if needed);

* it makes sure that names of output files are acceptable on all major
  platforms, that is, you can have a file with question mark `?` in its name
  on your Unix system, `wav2` will produce correct track title tag, but the
  file name itself will be converted so Windows users can copy the file too.

## Installation

This is a Python 3 script, you will need Python 3 installed to run it.

To install the software `cd` into the repository and execute the following:

```
# bash install.sh
```

Done. You can use `uninstall.sh` script to uninstall the software. Please
note that you'll need `flac` and/or `lame` to actually convert anything, so
install them too.

## Documentation

`wav2` comes with its own man page. Here is short synopsis:

```
usage: wav2 [-h] [-F] [-M] [-n] [-i] [-o OUT] [-l S] [-a S] [-c S] [-g S] [-y S]
            [--license] [--version]
            [FILE [FILE ...]]

Convert WAV files into FLAC and/or MP3 format

positional arguments:
  FILE                  file to process

optional arguments:
  -h, --help            show this help message and exit
  -F, --flac            convert FILE into FLAC format
  -M, --mp3             convert FILE into MP3 format
  -n, --count           count number of FILEs and write it as tag
  -i, --indexing        parse numeric prefix of filenames, store it as tag
  -o OUT, --output OUT  save converted files in OUT directory
  -l S, --album S       write S as «album» tag
  -a S, --artist S      write S as «artist» tag
  -c S, --comment S     write S as «comment» tag
  -g S, --genre S       write S as «genre» tag
  -y S, --year S        write S as «year» tag
  --license             show program's license and exit
  --version             show program's version number and exit
```

## Missing Features?

If you would like to see some new features in `wav2`,
[open an issue](https://github.com/mrkkrp/wav2/issues).

## License

Copyright © 2015 Mark Karpov

Distributed under GNU GPL, version 3.
