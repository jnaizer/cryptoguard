# Cryptoguard

## Overview

`cryptoguard` is a Python package designed for conducting comprehensive testing of random number generators. It provides a collection of testing suites that evaluate the statistical properties and reliability of random number sequences.

## Features

- Supports multiple testing suites, including ENT, PractRand, TestU01, Rabbit, Dieharder, and NIST STS.
- Offers predefined testing settings: Light, Recommended, All, and Custom.
- Allows custom selection of testing suites using binary representation.
- Stores the results in a user-specified directory.

## Installation

You can install the `cryptoguard` package using pip:

```bash
pip install cryptoguard
```

## Usage
Run the script using the command line:

```bash
cryptoguard [options]
```

### Options
- -v, --version: Show the version of the script.
- -l, --list-suites: List all available testing suites.
- -g, --list-settings: List all available testing settings.
- -b, --binary-file: Binary file to test.
- -s, --setting: Testing setting number. Options are:
  - 1: Light
  - 2: Recommended
  - 3: All
  - 4: Custom
- -i, --binary-setting: Binary representation of the tests to run (only for Custom setting).
- -d, --directory: Directory to store the results (will be created if it doesn't exist).

### Example
To test a binary file using the recommended settings and store the results in the results directory:

```bash
cryptoguard -b path/to/binary/file -s 2 -d results
```

### Custom Settings
For custom settings, you can use the -i option with a binary string. Each bit represents whether a particular test suite should be run (1) or not (0). The order of test suites is:

1. ENT
2. PractRand
3. SmallCrush
4. Crush
5. Alphabit
6. Rabbit
7. Dieharder
8. NIST STS

For example, to run ENT, PractRand, and Dieharder:

```bash
cryptoguard -b path/to/binary/file -s 4 -i 11000010 -d results
```

## Contributing
Contributions are welcome! Please submit a pull request or open an issue to discuss your ideas.

## License
This project is licensed under the MIT License. See the LICENSE file for details.

## Acknowledgements
This project was created as a part of my M.S. in Computer Science Thesis Report.

Contact
For any inquiries, please contact [jnaizer777@gmail.com].
