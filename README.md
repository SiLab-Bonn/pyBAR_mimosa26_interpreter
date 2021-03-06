
# Mimosa26 Interpreter [![Build Status](https://travis-ci.org/SiLab-Bonn/pymosa_mimosa26_interpreter.svg?branch=master)](https://travis-ci.org/SiLab-Bonn/pymosa_mimosa26_interpreter) [![Build status](https://ci.appveyor.com/api/projects/status/6ur82s62x9hs7mj4?svg=true)](https://ci.appveyor.com/project/laborleben/pymosa-mimosa26-interpreter)


pymosa_mimosa26_interpreter - A Mimosa26 raw data interpreter in Python.

Interpreter for [Mimosa26](http://www.iphc.cnrs.fr/List-of-MIMOSA-chips.html) raw data recorded with [pymosa](https://github.com/SiLab-Bonn/pymosa) DAQ.

The events are built by using the trigger words in the raw data generated by the [TLU FSM](https://github.com/SiLab-Bonn/basil/tree/master/basil/firmware/modules/tlu). It is also possible to create a PDF with an occupancy map for each Mimosa26 plane.

**Note:**
The parameter `DATA_FORMAT` must be set to 2 (15 bit trigger number + 16 bit trigger timestamp) in the TLU FSM so that the interpreter can work.

## Installation

The following packages are required for the Mimosa26 interpreter:
```
matplotlib numba numpy pytables tqdm
```

Then install the Mimosa26 interpreter:
```
pip install .
```

## Usage

An example script which does the raw data interpretation as well as the creation of a hit table
is located in the [`examples`](https://github.com/SiLab-Bonn/pymosa_mimosa26_interpreter/blob/master/examples/) folder. The ouput file can be used with [Beam Telescope Analysis (BTA)](https://github.com/SiLab-Bonn/beam_telescope_analysis).

## Support

Please use GitHub's [issue tracker](https://github.com/SiLab-Bonn/pymosa_mimosa26_interpreter/issues) for bug reports/feature requests/questions.
