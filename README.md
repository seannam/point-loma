# Point Loma
A Python script to execute Lighthouse and export results.
version 0.2

## Requirements
- lighthouse (Node package) 
See below for installation instructions

- Chrome Canary 
Needed for headless mode, which is not yet implemented

setup.py should install the Python depencies 
- sh (Python package)
- click (Python package)
- pathlib (Python package)

Installing [Lighthouse]("https://github.com/GoogleChrome/lighthouse")
*Lighthouse requires Node 6 or later.*

**Installation:**

    npm install -g lighthouse
    # or use yarn:
    # yarn global add lighthouse


## Setup
1. Download Google Chrome for Desktop.
2. Install the current [Long-Term Support](https://github.com/nodejs/LTS) version of [Node](https://nodejs.org/).
3. Install Lighthouse. See above for quick start instructions or link for more details.

## Usage
Usage: pointloma [OPTIONS] LINK

  This script runs Lighthouse using the command line interface.

Options:

    --count INTEGER  Number of tests to run. Default is 1.
	--output-file TEXT  Name of csv file w/o extension. Default is "output".
	--help           Show this message and exit. 

## Output
Each test will output to a HTML and json file, named *resultsN.report.html* and *resultsN.report.json*, where *N*, is the test number.
Unless specified, a csv file named 'output.csv' will contain four performance metrics and the average of all tests. If the number of tests is one, the average will not be printed.

## Coming Soon
- Run in chrome headless mode
- Choose name for generated HTML and JSON reports