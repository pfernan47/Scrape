# scrape.hs

* Paola Fernandez Lopez - pfernan4(at)eafit(dot)edu(dot)co
* Juliana Vallejo Diez - jvalle22(at)eafit(dot)edu(dot)co

## Program description:
The `Main` module extracts the HTML code from an input URL and scrapes it
to find its bibliographic production, which is later saved on a .tsv document.
The .tsv document will contain for each publication : type of publication,
author, publication's name and validation.

This module was designed only for input URLs from the GrupLAC platform and we
do not guarantee it will work on other platforms.

When using the program you may have some problems related with internet
connection. If so, the program will return  "empty list" when using it.
Please make sure you have a stable connection and reload the module to
solve the problem.

## Requirements
This module requires the download package of cabal.

## Usage:
Load the module with:
`ghc scrape.hs``
This will create an executable file for the module. To execute it, use:
`.\scrape`
and write the URL, like this:
`$./scrape
$http://scienti.colciencias.gov.co:8080/gruplac/jsp/visualiza/visualizagr.jsp?
  nro=00000000004135``
This will automatically create a .tsv file in your working folder. If you want
to display the .tsv file you can use `head` ,`tail` or `cat` followed by the
file name, like this: `$ head "Logica-y-Computacion.tsv"``

* GHC, version 8.0.2
* Haskell Platform 8.0.2
* MacBook Air, macOS Sierra version 10.12.6
