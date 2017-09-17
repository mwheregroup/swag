# Swag

Color your shell output with escape code magic.

![Demo](https://media.giphy.com/media/l0O5ASEoXnoaMd3S8/source.gif)

## Installation

`pip install swag`

## Usage


```
usage: swag [-h] {print,install} ...

positional arguments:
  {print,install}  [command] help
    install        install the colors to the folder of choice
    print          prints the text with the specified color and type to the
                   console

optional arguments:
  -h, --help       show this help message and exit
```

## Raw Usage



### Use from code

```
from swag import colors
print colors.COLORS["red"], "This will be red"

# Or use the SwagPrinter class:

from swag.swagprinter import SwagPrinter, INTENSE

printer = SwagPrinter()
printer.print_green("Blah", INTENSE) # Prints an intense green

# Prints an intense green, to the end of the output:
printer.print_green("Blah", INTENSE, true)

```

### Installation to a folder

From the commandline do

```
swag install -d <path/to/folder> # default is ~/.colors
```

This will install all the escape codes to the ~/.colors or <path/to/folder> folder.

Now you can use the colors directly from the console via:

`echo $(cat ~/.colors/blue) This will be blue`
