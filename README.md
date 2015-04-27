# Smart Converter from WAV to FLAC and/or MP3 format

*Under development, nothing to try yet.*

This script can convert `*.wav` files into FLAC or MP3 format using `flac`
or `lame` encoders respectively. Main features:

* when file name has numeric prefix it parses it and writes it as «tract
  number» tag;

* it can automatically count total number of supplied files and write this
  number as «total tracks» tag;

* it accepts various options like «album artist» and «album name» and passes
  them to corresponding encoder, this way you don't need to remember
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

`wav2` comes with its own man page.

## License

Copyright © 2015 Mark Karpov

Distributed under GNU GPL, version 3.
