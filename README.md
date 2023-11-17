```
┏━╸╻┏━╸╻  ┏━╸╺┳╸   ┏━╸┏━┓┏┓╻╺┳╸┏━┓
┣╸ ┃┃╺┓┃  ┣╸  ┃    ┣╸ ┃ ┃┃┗┫ ┃ ┗━┓
╹  ╹┗━┛┗━╸┗━╸ ╹    ╹  ┗━┛╹ ╹ ╹ ┗━┛
```

My collection of ascii art fonts for [figlet](http://www.figlet.org/) or [toilet](http://caca.zoy.org/wiki/toilet). 

# Getting Started
## Requirements

* [figlet](http://www.figlet.org/)
* a CLI (if you're on Windows, this is the Command Prompt; for Linux and Mac, this is your Terminal)

## Installing Fonts
Run the following command in your CLI to install all fonts in this repository to your figlet fonts directory:

`wget https://github.com/xero/figlet-fonts/archive/master.zip && sudo unzip -j master.zip -d "$(figlet -I 2)" && rm master.zip`

This command will download the latest version of this repository, unzip it, and install all fonts to the right figlet fonts directory. 

If you want to install a specific font, you can download it from the [fonts](fonts) directory and place it in your figlet fonts directory (output of `echo "$(figlet -I 2)"`).

If you want to see examples of the fonts before installing anything to your Figlet fonts directory, proceed to the next section.

## Viewing Examples of each Font 
You can view examples of each font at [examples](fonts/Examples.md). However, if you want to see a consistent sample message for each font on your terminal, you can run a simple command.

Wihtout copying all the contents to your Figly fonts directory clone this repo wherever you'd like. From the root directory (i.e. `figlet-fonts/``), run the following command:

`for file in ./examples/*.txt; do if [ -f "$file" ]; then echo "Contents of $(basename "$file"):"; cat "$file"; echo "-----------------------"; fi; done`

This will print `this is an example` in each font.

If you are using something like [lolcat](https://github.com/busyloop/lolcat) to further stylize, then you can ammend the command to look like this:

`for file in ./examples/*.txt; do if [ -f "$file" ]; then echo "Contents of $(basename "$file"):"; cat "$file" | lolcat; echo "-----------------------"; fi; done`

Be warned that using lolcat with this command greatly increases the time it takes to run.
