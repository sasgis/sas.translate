
This repository contains the localization files for the SAS.Planet application.

The names of the localization files correspond to the two-letter codes [ISO 639-1](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes):
- `es.po` - Spanish
- `fa.po` - Persian (Farsi)
- `fr.po` - French
- `ru.po` - Russian
- `tr.po` - Turkish
- `uk.po` - Ukrainian

The `default.po` file contains all strings in English that are used in the application. This file is generated automatically by a script.

The `ignore.po` file contains strings that appear in the application but are not to be translated (this file is used by scripts). You can add strings to this file as needed.

Scripts to generate the `default.po` and update the `xx.po` files from the application sources can be found here: https://github.com/sasgis/sas.translate.dev
