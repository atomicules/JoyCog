#JoyCog

A little learning exercise in [Joy](http://www.kevinalbrecht.com/code/joy-mirror/index.html). It's a "trivial" (It wasn't for me!) programme that takes a list of (two) chainset gears and a list of sprockets and then calculates all the ratios reporting out the results as a sorted list of ratios and gear pairs:

	> [34 50] [12 13 15 17 19 21 23 26] joycog.
	> [[1.30769 26 34] [1.47826 23 34] [1.61905 21 34] [1.78947 19 34] ... ]

I decided to do this as I was intrigued about what the theoretical progression of gears should be on my bike (you could never shift like this in practice). There is more overlap than I thought.

One possible extension I could do is to discount the ratios at the extremes of chain angle, e.g. biggest front geat and biggest rear sprocket. But wrapping my head around Joy has been hard, so I'll not do that too soon.

##Installing / Using

1. Get and compile Joy from [Kevin Albrecht's mirror](http://www.kevinalbrecht.com/code/joy-mirror/index.html) (I went with "current joy.tar.gz")

###Interactively

2. Start an interactive Joy session from within the directory where joy was compiled so that usrlib, inilib and agglib are loaded automatically, e.g: `./joy`
3. Import joycog like so: `/path/to/joycog.joy include.`
4. Run as `[34 50] [12 13 15 17 19 21 23 26] joycog.`

###From the Command Line

5. Edit the relative path in the joycogcl.joy file
6. cd to the joy executable directory (so usrlib, inilib and agglib are loaded automatically)
7. Call as `./joy /path/to/joycogcl.joy 34 50 12 13 15 17 19 21 23 26`. I.e the first two arguments are the front chainring the rest are the cassette
