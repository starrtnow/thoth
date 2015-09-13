### thoth
Making epubs from web pages.

####Depedencies
The only dependency is NSoup, which is a port of JSoup to .net. Of course, the .net runtime is required as well.

####Usage

thoth is intended to be used as a command line program, but works as just an executable as well, though some flexibility is lost. There are three main ways to feed in urls:

1. An index file on the internet

  If you input no arguments, or one argument with the -w flag, then the uri will be downloaded and all of the anchor tags on the page will be printed out with their respective index listed next to them. Input a range delimited with a comma (i.e, "4,10") and the urls in that range will downloaded.
  
2. A list of urls delimited by spaces in a local file

  If you input exactly one argument without the -w flag, then the program will attempt to read in the file and download the urls in it, delimited by newlines.

3. Arguments

  If multiple arguments are inputted, then those will be downloaded. 
  
#####Flags

* -a Author — Sets the author
* -t Title— Sets the title
* -c CoverUrl.jpg — Sets the cover
* -w — Downloads the argument as index

####FAQ

* Why is it called thoth?

    Something something patron god of scribes something. Also carried me through the midgame of Persona 4. 

* I want to change the default cover picture

    Swap Cover/Cover.png with whatever you want. It has to end with .png, because I'm lazy.

* I want to compile this.

  Okay. It should compile fine in either mono or microsoft's f# compiler. The (basic) makefile I used is even there.
  
* X-thing broke!

  Well, that's not good. Make an issue and I'll try to fix it. Sometimes, though, I won't have time.

* I want X-feature!
  
  Okay. Tell me, I'll try. It is open source, feel free to add it in yourself.
  
* Why is this written in F#?
  
  Because I wanted to learn a ML-derived language

* Does this work on Linux/OSX?

  Actually, it does. I developed it mostly in mono on linux. You do need v4.0 of the mono runtime because ZipFile wasn't implemented till then.
  
* Why is there so little epub metadata configuring?

  Because I'm lazy.
  
* Why no GUI?

  Because GUIs are hard and I'll have to use an imperative library to do it and I'll actually have to with runtime errors.
  
* Why not the HTMLAgilityPack?

  Three reasons:
    1. There apparently isn't online documentation. Wat. At least NSoup is basically verbatim JSoup, so I can use their docs.
    2. License. Not a big deal, but NSoup is under a more permissive license.
    3. Up-to-date-ness. Apparently the HTMLAgilityPack hasn't been updated since 2012. Wat.
    




