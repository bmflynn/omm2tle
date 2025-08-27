# omm2tle

A tool to convert CCSDS OMM (Orbit Mean-Elements Message) files to TLE (Two-Line Element) format.

This tool supports OMM XML or NDM (Navigation Data Message) XML files containing one or more 
OMMs.

Requires:

  * Python >= 3.6

References:

  * [CCSDS OMM Specification](https://public.ccsds.org/Pubs/502x0b2c3.pdf)
  * [TLE Format Description](https://en.wikipedia.org/wiki/Two-line_element_set)

## Usage
```
$ ./omm2tle -h
usage: omm2tle [-h] [--test] [-m MAP] [--2le] [-i INPUT]

Convert CCSDS Orbital Mean Message (OMM) XML to Two-Line Element (TLE) format.

Project: https://github.com/bmflynn/omm2tle

options:
  -h, --help            show this help message and exit
  --test                Run self-test and exit
  -m MAP, --map MAP     Map any NORAD catalog ids > 99999 to this value. This may be useful if the default alpha-5 (alphanumeric) format is not desired.
  --2le                 Output 2LE format rather than 3LE format (with title line)
  -i INPUT, --input INPUT
                        Input OMM or NDM XML file. Read from stdin if '-'
```

## License 

Licensed under

 * MIT license ([LICENSE-MIT](LICENSE-MIT) or http://opensource.org/licenses/MIT)
