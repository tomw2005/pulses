# MetaPost MRI pulse sequence macros

These MetaPost macros draw simple but publication-quality MRI pulse
sequence diagrams for TeX documents, by describing RF and gradients
events as a series of logical objects along lines.

This a fork of [the pulses macros by Mark White](https://bitbucket.org/mjwhite/pulses),
which was [originally published in 2004](http://www.celos.net/comp/pulses/).

Impoved gradient shapes have been added as per [Proper Gradients for Metapost Pulse Sequences](http://www.tinkertailorsoldiersponge.com/blog/2013/12/18/proper-gradients-for-metapost-pulse-sequences).

## Usage

Macros are in 
[pulses.mp](https://bitbucket.org/mjwhite/pulses/src/default/pulses.mp).
Several example sequences are in
[seq.mp](https://bitbucket.org/mjwhite/pulses/src/default/seq.mp).

Many TeX installations come with MetaPost so you might well have it
already. Running `mpost seq.mp` will create a series of numbered
postscript fragments, one for each figure, suitable for inclusion with
TeX or LaTeX.

Getting fonts right in MetaPost can be complex. Depending on your
installation and how you want to use the output, you may need to
comment or change the `prologues` and `defaultfont` lines at the top of
`pulses.mp` and/or the `infont "Symbol"` lines in `seq.mp`.

If you're an MRI scientist (which I guess you are, if you've made it
this far down the page) you may notice that figure 2 has a physics
error: the readout gradient starts during the excitation pulse.
Fortunately somebody spotted that in the draft these came from.

There is a write-up on the installation and basic use on [my blog](http://www.tinkertailorsoldiersponge.com/blog/2013/12/17/pulse-sequence-diagrams-using-metapost)

## Examples
Basic FLASH sequence using the original gradients:
![alt tag](http://lh5.googleusercontent.com/-HnS9_Sbu2fw/UrCYazM9qtI/AAAAAAAAAzk/nNDmMc-wp1U/w1003-h881-no/flash.png)
Spin Echo sequence with the improved gradients:
![alt tag](http://lh6.googleusercontent.com/-pWAgfVprTUY/UrHUqtlcpSI/AAAAAAAAA0U/6kttxxCOI9s/w1140-h881-no/se_grads.png)
## Author

Written by Mark White, mark [at] celos.net, in 2004.

There didn't seem to be many straightforward tools for this in 2004,
so I published the files online
[here](https://bitbucket.org/mjwhite/pulses) 
with some examples and comments. In 2016 I released the same code
under a clear 2-clause BSD licence here.

The 2016 release (1.0) is identical apart from a few lines in the
header comments referring to the licence. Thir version (1.1) has improved gradient shapes.  

## Licence and contact

Both files - the macros and the example sequence diagrams (which were
taken from a draft of my PhD thesis) - are released under the 2-clause
BSD licence. See 
[COPYING.txt](https://bitbucket.org/mjwhite/pulses/src/default/COPYING.txt)
in the distribution for details.

If you do anything useful with this code, or if you have any comments
or patches, I'd love to hear from you - email mark [at] celos.net.
