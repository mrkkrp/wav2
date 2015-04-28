# WAV2 FLAC and/or MP3 format

This script can convert `*.wav` files into FLAC or MP3 format using `flac`
or `lame` encoders respectively. Main features:

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

* output directory can be specified (and created if needed).

## Installation

Just execute:

```
# bash install.sh
```

Done. You can use `uninstall.sh` script to uninstall the software. Please
note that you'll need `flac` and/or `lame` to actually convert anything, so
install them too.

## Documentation

`wav2` comes with its own man page. Here is short synopsis:

```
wav2 — convert WAV files into FLAC and/or MP3 format

Usage: wav2 [OPTIONS] [FILES]

Available options:
  -h,--help                Show this help text
  -F,--flac                Convert FILES into FLAC format
  -M,--mp3                 Convert FILES into MP3 format
  -n,--count               Count number of FILES and write it as tag
  -o,--output OUT          Save converted files in OUT directory
  -i,--indexing            Parse numeric prefix of files and write as tag
  -l,--album STR           Write STR as «album» tag
  -a,--artist STR          Write STR as «artist» tag
  -c,--comment STR         Write STR as «comment» tag
  -g,--genre STR           Write STR as «genre» tag
  -y,--year STR            Write STR as «year» tag
  --license                Show license of the program
  --version                Show version of the program
```

## Missing Features?

If you would like to see some new features in `wav2`,
[open an issue](https://github.com/mrkkrp/wav2/issues).

## License

Copyright © 2015 Mark Karpov

Distributed under GNU GPL, version 3.
