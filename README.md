# xml-bible

The xml-bible is adapted from the [WEB Bible](http://ebible.org/web/) which is a [Public Domain](http://ebible.org/web/copyright.htm) Bible translation.  I modified their [USFX Format](http://ebible.org/eng-web/eng-web_usfx.zip) for easier parsing.

The xml-bible is not meant as a resource for proper textual representation or formatting of the Biblical text.  Instead it is simply meant to be a bare-bones book/chapter/verse representation of the text.  For a more stylistically comprehensive format of the Bible look [here](http://ebible.org/usfx/Bible-encoding.htm).

The master branch has the entire Bible in one massive xml file.  If you would rather work with smaller files the [by_book](https://github.com/philosowaffle/xml-bible/tree/by_book) branch has the books broken out into separate files.

<a href="https://www.buymeacoffee.com/philosowaffle" target="_blank"><img src="https://www.buymeacoffee.com/assets/img/custom_images/black_img.png" alt="Buy Me A Coffee" style="height: 41px !important;width: 174px !important;box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;-webkit-box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;" ></a>

## Parsing with XPath

Here are a few [XPath](https://www.google.com/webhp?sourceid=chrome-instant&rlz=1C1LENP_enUS639US639&ion=1&espv=2&ie=UTF-8#q=xpath) examples for parsing different types of data from the xml-bible.

### Book
````
/root//book[@id="GEN"]//v/text()
````

### Chapter
````
/root//book[@id="GEN"]//c[@id="1"]//v/text()
````
Multiple Chapters;
````
/root//book[@id="GEN"]//c[@id >= "1" and @id <= "3"]//v/text()
````

### Verse
````
/root//book[@id="GEN"]//c[@id="1"]//v[@id="1"]
````
Multiple Verses:
````
/root//book[@id="GEN"]//c[@id="1"]//v[@id >= "1" and @id <= "3"]/text()
````

## Book Codes
````
genesis = GEN
exodus = EXO
leviticus = LEV
numbers = NUM
deuteronomy = DEU
joshua = JOS
judges = JDG
ruth = RUT
1st samuel = 1SA
2nd samuel = 2SA
1st kings = 1KI
2nd kings = 2KI
1st chronicles = 1CH
2nd chronicles = 2CH
ezra = EZR
nehemiah = NEH
esther = EST
job = JOB
psalms = PSA
proverbs = PRO
ecclesiastes = ECC
song of solomon = SNG
songs of solomon = SNG
song of songs = SNG
isaiah = ISA
jeremiah = JER
lamentations = LAM
ezekiel = EZK
daniel = DAN
hosea = HOS
joel = JOL
amos = AMO
obadiah = OBA
Jonah = JON
micah = MIC
nahum = NAM
habakkuk = HAB
zephaniah = ZEP
haggai = HAG
zechariah = ZEC
malachi = MAL
matthew = MAT
mark = MRK
luke = LUK
john = JHN
acts = ACT
romans = ROM
1st corinthians = 1CO
2nd corinthians = 2CO
galatians = GAL
ephesians = EPH
philippians = PHP
colossians = COL
1st thessalonians = 1TH
2nd thessalonians = 2TH
1st timothy = 1TI
2nd timothy = 2TI
titus = TIT
philemon = PHM
hebrews = HEB
james = JAS
1st peter = 1PE
2nd peter = 2PE
1st john = 1JN
2nd john = 2JN
3rd john = 3JN
jude = JUD
revelation = REV
````
