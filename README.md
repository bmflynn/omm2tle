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
usage: omm2tle [-h] [--test] [-m MAP_ID] [--2le] [-i INPUT]

Convert CCSDS Orbital Mean Message (OMM) XML to Two-Line Element (TLE) format.

See https://public.ccsds.org/Pubs/502x0b2c3.pdf for the OMM specification.

options:
  -h, --help            show this help message and exit
  --test                Run self-test and exit
  -m MAP_ID, --map-id MAP_ID
                        Maps one NORAD catalog to another. This may be necessary if the catalog id is greater than 99999 and the default alpha-5 (alphanumeric) format is not desired. Values specified here must be in the format <original>=<new>, e.g. 25544=12345. Multiple mappings may be specified by repeating this option.
  --2le                 Output 2LE format rather than 3LE format (with title line)
  -i INPUT, --input INPUT
                        Input OMM or NDM XML file. Read from stdin if '-'`sh
```

## License 

Licensed under

 * MIT license ([LICENSE-MIT](LICENSE-MIT) or http://opensource.org/licenses/MIT)
