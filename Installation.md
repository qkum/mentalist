# Prebuilt Applications

The easiest way to get up and running with Mentalist is to use the prebuilt applications, which are available for Linux, OS X and Windows on the [Mentalist releases page](https://github.com/sc0tfree/mentalist/releases).

# Install from Source

## Prerequisites

#### Linux (APT package manager)

Check if Python 3 is installed by running `python3 --version`. If it is not, run:

`sudo apt-get update && apt-get install python3.6`

Additionally, you will need setuptools and Tk:

`sudo apt-get install python3-setuptools python3-tk `

#### OS X

There are varying ways of installing Python 3 on OS X, but the easiest is to install through [Homebrew](https://brew.sh/).

`brew update && brew install python3`

#### Windows

If using Windows, please refer to [Installing Python 3 on Windows](http://docs.python-guide.org/en/latest/starting/install3/win/) from the Hitchhiker's Guide. It is also _extremely helpful_ to click the Python 3 installer checkbox to add Python to your PATH.

## Install Mentalist

Clone the Mentalist repository:

`git clone https://github.com/sc0tfree/mentalist.git`

Go into the directory:

`cd mentalist`

Run setup.py:

`python3 setup.py install`

## Running Mentalist

You can now run mentalist from the shell with the command `mentalist`.

# Rebuilding Applications

It is possible to rebuild the applications from source using PyInstaller. First, install PyInstaller:

`pip3 install pyinstaller`

To build the application for your current operating system, execute:

`pyinstaller --onefile --windowed mentalist.spec`

_Note: Make sure that `pyinstaller` in your path refers to the Python 3 version and not Python 2!_

Once completed, you can find the executable in the `dist` directory.

### OS X building:

You must have the [Homebrew](https://brew.sh/) version of Python 3 to compile an OS X application. The [python.org](https://www.python.org/) version will fail for building.

### Linux building:

Make sure to install pip3 and Tk with:

`sudo apt-get install python3-tk python3-pip`

# Running Tests

To run tests, use `python3 setup.py test`