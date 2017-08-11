## An MDG minuet created by `mdginabc2svg.sh`
Clicking (tapping for mobile users) on image will consequently play the music. 

<script src='./samples/js/abc2svg-1.js' type='text/javascript'></script>
<script src='./samples/js/abcemb-1.js' type='text/javascript'></script>
<script src='./samples/js/play-1.js' type='text/javascript'></script>
<style type='text/css'>
	svg {display:block}
</style>

<center>
%abc-2.2
%<![CDATA[
%%scale 0.75
%%pagewidth 21cm
%%bgcolor white
%%topspace 0
%%composerspace 0
%%leftmargin 0.80cm
%%rightmargin 0.80cm
X:189874916791621
T:7-7-7-7-7-7-7-7-7-7-7-7-7-7-7-7
%%setfont-1 Courier-Bold 12
T:$1K.516f::104:157:27:167:154:68:118:91:138:71:150:29:101:162:23:151::$0
T:$1Perm. No.: 189874916791621$0
M:3/8
L:1/8
Q:1/8=111
%%staves [1 2]
V:1 clef=treble
V:2 clef=bass
K:C
%1
[V:1]|: e/d/e/g/c'/g/ |\
[V:2]|: C,2z |\
%2
[V:1] e/d/e/g/c'/g/ |\
[V:2] C,2z |\
%3
[V:1] f/e/f/d/c/B/ |\
[V:2] [B,2G,2]z |\
%4
[V:1] cc/d/e |\
[V:2] [E,2C,2]z |\
%5
[V:1] d/^c/d/^f/a/f/ |\
[V:2] C,2z |\
%6
[V:1] gb/g/d/g/ |\
[V:2] B,,2z |\
%7
[V:1] e/a/g/b/^f/a/ \
[V:2] C,D,D,, \
%8a
[V:1]|1 [g2d2B2G2]z :|2
[V:2]|1 G,,G,/=F,/E,/D,/ :|2
%8b
[V:1] [g2d2B2G2]z |:\
[V:2] G,,B,/G,/^F,/E,/ |:\
%9
[V:1] [^fdA]!trill!f2 |\
[V:2] D,,/D,/^C,/D,/^C,/D,/ |\
%10
[V:1] g/b/d'/b/g |\
[V:2] [D,2B,,2][D,B,,] |\
%11
[V:1] [ecG]!trill!e2 |\
[V:2] C,/B,,/C,/D,/E,/^F,/ |\
%12
[V:1] B/d/g/d/B |\
[V:2] G,2G,, |\
%13
[V:1] e/d/e/g/c'/g/ |\
[V:2] G,2 E, & C,2 C, |\
%14
[V:1] e/d/e/g/c'/g/ |\
[V:2] [G,2C,2][E,C,] |\
%15
[V:1] f/e/d/e/f/g/ |\
[V:2] A,/G,/F,/G,/A,/B,/ |\
%16
[V:1] c2z :|]
[V:2] C,G,,C,, :|]
%]]>
</center>


## mdginabc2svg.sh
[**mdginacb2svg.sh**](https://github.com/justineuro/mdginabc2svg) is a [Bash](https://www.gnu.org/software/bash/) script [(see Wikipedia:Bash_(Unix_shell)](https://en.wikipedia.org/wiki/Bash_%28Unix_shell%29) for more info) than can be used for creating an XHTML file containing the score of a particular [Musical Dice Game (MDG)](https://en.wikipedia.org/wiki/Musikalisches_W%C3%BCrfelspiel) minuet, generated based on the rules given in  [Musikalisches Würfelspiel, K.516f (Mozart, Wolfgang Amadeus)](http://imslp.org/wiki/Musikalisches_W%C3%BCrfelspiel,_K.516f_(Mozart,_Wolfgang_Amadeus)).  The generated XHTML file contains the musical score for an MDG written in [ABC](http://www.abcnotation.com) music notation and is rendered using [Jeff Moine's `abc2svg` javascripts (v. 1.13.6; 2017-08-08)](http://moinejf.free.fr/js/index.html).  To view the generated musical score, open it in a javascript-enabled web browser; to listen to the corresponding music, simply click (or tap, for mobiles) on the image of the musical score inside the browser (reload the page to prematurely stop).

The [GitHub mdginabc2svg](https://github.com/justineuro/mdginabc2svg) directory includes:

* `mdginabc2svg.sh` - a Bash script for generating the MDG minuets corresponding to any sequence of 16 tosses of a pair of dice
* `mdginac2svg-sm.sh` - similar to `mdginabc2svg.sh` but smaller SVG images are created
* `mdginac2svg-tab2.sh` - similar to `mdginabc2svg.sh` but coded with tabs of length 2
* `samples` - a folder containing samples of generated MDG minuets as XHTML files and a sub-folder containing the needed javascripts for rendering the minuet written in ABC notation as SVG images.

To use the Bash script, at the command line type:

```
/path/to/mdginabc2svg.sh n1 n2 n3 n4 n5 n6 n7 n8 n9 n10 n11 n12 n13 n14 n15 n16
```
    
where `n1, n2, ..., n16` are any of the 11 possible outcomes of the toss of two ordinary six-sided dice, e.g., are 16 integers, not necessarily unique, chosen from the set {2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12}.  For example, if the script is located in the present working directory and each outcome of the 16 dice tosses was a 3:

```
./mdginabc2svg.sh 3 3 3 3 3 3 3 3 3 3 3 3 3 3 3 3
```
The output will be the file `K516f-3-3-3-3-3-3-3-3-3-3-3-3-3-3-3-3.xhtml`, containing the score of the MDG minuet corresponding to the 16 outcomes given at the command line (all tosses came up a 3), and will be created under the current working directory.  Please see the `samples` folder in this directory for more sample XHTML files.

## More examples
Please find more examples in the [samples page](../samples/index.md).

## Acknowledgements
My sincerest gratitude to Jeff Moine for [abc2svg](http://moinejf.free.fr/js/index.html) and the accompanying useful javascripts, examples, templates, and pointers for the appropriate use of these resources. Guido Gonzato for the [ABC Plus Project](http://abcplus.sourceforge.net/) and the [abcmidi resources](http://abcplus.sourceforge.net/#abcMIDI) available there, more especially for the ABC resource book *Making Music with ABC 2*.  Special thanks also to the [International Music Score Library Project (IMSLP)](http://imslp.org/) for making available the score for *Musikalisches Würfelspiel, K.516f*.

## License
<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/80x15.png" /></a><br /><span xmlns:dct="http://purl.org/dc/terms/" property="dct:title"><b>mdginabc2svg</b></span> by <a xmlns:cc="http://creativecommons.org/ns#" href="https://github.com/justineuro/mdginabc2svg" property="cc:attributionName" rel="cc:attributionURL">Justine Leon A. Uro</a> is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.<br />Based on a work at <a xmlns:dct="http://purl.org/dc/terms/" href="https://github.com/justineuro/mdginabc2svg" rel="dct:source">https://github.com/justineuro/mdginabc2svg</a>.