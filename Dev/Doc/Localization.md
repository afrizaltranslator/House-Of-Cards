# Localization

Now the game is very easy to localize to any language using the Romanic alphabet.

The files for the languages are stored in the [SRC/Assets/Tricky/Lang](https://github.com/PhantasarProductions/House-Of-Cards/tree/main/SRC/Assets/Tricky/Lang) folder.
The file should just have the ENGLISH name of your language suffixed with .ini

Now the first lines of the ini file should look like this
~~~ini
[^SYS^]
ACTIVE=Yes
CREATIONDATE=2/2/2024 10:18:07 AM
CREATIONTOOL=Rosetta
~~~
[^SYS^] just just be present at the top and then the field ACTIVE should always be "YES" (or some versions of the game might ignore this localization). CREATIONDATE should contain the date and time you started to work on that file. The format you use is not really that relevant, but having this all in the same format will give a better organized look, I think.
The field CREATIONTOOL should just be the editor you used. Could be NotePad++ could be anything, but remember, it must support the Unix LF text format. The Windows CRLF format WILL cause the game to malfunction. Now I can convert all this quite easily, and this GitHub Repository is even configured to that, but it'll save some trouble to keep it in mind, anyway.

Then the next block
~~~ini
[LANGUAGE]
NAME=English
TRANSLATOR=Jeroen P. Broks
~~~
In the [LANGUAGE] section the "NAME" variable should contain the name of your language is the actual language. So in an Italian translation it should not say "Italian" but "Italiano", and you will also see that in the Dutch.ini file the name contains "Nederlands" which is the Dutch name for the Dutch language.
In the field "TRANSLATOR" you fill in your name. 

An basically all other fields should just contain the translation into your language.

# Special characters

The game only supports ASCII based files, and that basically blocks out the usages of accent marks (such as è and é), umlauts (such as ü) and other special characters. You can write them anyway with writing a | and then the next two characters can decide the special character.
Please note, when the font does not have a character for the combination you typed the request will be ignored.
Here is a list of the codes currently supported
Char | Code
-----|------
é    | \|'e
è    | \|`e
ä    | \|ua
ë    | \|ue
ö    | \|uo
ü    | \|uu
ß    | \|ss
â    | \|^a
ç    | \|'c
In most cases having the second character after the \| upper case should give you the upper case variant (but no guarantees).
