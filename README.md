# Golden-Even

This repository contains code and source files for building a dictionary of Even language. It is based on the data from the dictionary of V. A. Robbek and M. Je. Robbek. The online version is available on [http://jazykirossii.ru/eve.html](http://jazykirossii.ru/eve.html).

In order to run the application one should download a version of GoldenDict which allows to add custom scripts. The current application was developed and tested on Windows with GoldenDict 1.5.0. It is higly likely that necessary versions are stored here:
 * [Windows](https://sourceforge.net/projects/goldendict/files/early%20access%20builds/)
 * [Mac](https://sourceforge.net/projects/goldendict/files/early%20access%20builds/MacOS/)

If you are a Linux user, find a correct version yourself, I believe in you.

After GoldenDict is installed, go to its directory and create two folders `dic` and `scripts` (actually, they can be anywhere on your computer but it is quite nice to keep them nearby the main programme). The next step is to fill the folders with the content of the current repository.

In the `dic` folder you can find a dictionary of Even in `.dsl` format. It contains **13 810** words. Add `dic` folder in GoldenDict: `Edit > Dictionaries > Files > Add > now choose widely` (`Правка > Словари > Файлы > Добавить`).

`scripts` folder contains 2 scripts:
 * `full_text.py` allows for searching within dictionary entries (full text search). To enable it, one should begin the input with `|`.
 ![full_text.png]

 * `substring.py` allows one to search lemmas by substring, not just the begining of the word. Do not forget to press Enter to enable this type of search!
 ![substring.png]

 
To activate the scripts you should open GoldenDict, go to `Edit > Dictionaries > Programs` (`Правка > Словари > Программы`) and add 2 lines (both HTML type).

 * `/path/to/your/python "path/to/GoldenDict/scripts/full_text.py" %GDWORD% "path/to/GoldenDict/dic/dictionary.dsl"`
 * `/path/to/your/python "path/to/GoldenDict/scripts/substring.py" %GDWORD% "path/to/GoldenDict/dic/dictionary.dsl"`

**NB!** Yes, you must have Python 3 installed. Sorry for that :(

Then enable both programmes and everything should work fine.

P.S. `Even.json` is a json version of the dictionary appeared as a by-product of building the application.