# friggeri-ubuntu
Friggeri-CV modified to work with Ubuntu and texlive-base.

## Synopsis
Someone close to me really wanted this CV template, which can be really complicated to use due the excessive number of dependecies. To make it work, I added a lot of its dependecies and modified the font used. 

## Installation
Aside from this repository you will need the following packages:

    sudo apt-get install texworks latex-xcolor texlive-xetex biber tex-gyre texlive-fonts-recommended

Since I use texworks, it will install texlive-base as a dependecy. Texworks will automatically identify xelatex but it will not identify biber (if you will like to use the bibliography), you need to manually add it in the Preferences (Edit->Preferences->Typesettings, add Processing Tool in /usr/bin/biber, use Argument $basename). 

## Usage
You will only need to modify 3 files:

- cv_10.xtx : Where the personal data actually is.
- friggeri-cv.cls : Configuration file, where you can change colors and fonts.
- ref.bib : Bibliography file.

In TeXworks, you should be able to sucessfully compile with xelatex. One important thing to note: if you gonna use the bibliography, you should:

- Compile once with xelatex.
- Use biber (check if your file was parsed correctly).
- Compile one or two more times with xelatex.
