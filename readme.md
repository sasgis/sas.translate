
This repository contains the localization files for the SAS.Planet program.

The names of the localization files correspond to the two-letter codes [ISO 639-1](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes):
- `es.po` - Spanish
- `fr.po` - French
- `ru.po` - Russian
- `uk.po` - Ukrainian

The `default.po` file contains all strings in English language that are used in the program. This file is generated automatically by script.

The `ignore.po` file contains strings that appear in the program but are not to be translated (this file is used by scripts). You can add strings to this file as needed. 

Scripts to generete the `default.po` and update the `xx.po` files can be found here: https://github.com/sasgis/sas.translate.dev