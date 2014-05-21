# MEI Customisations for Transforming Musicology

Contains customisations of [MEI](http://music-encoding.org/home) used
in the
[Transforming Musicology](http://www.transforming-musicology.org/)
project.

Currently these comprise just:

=instruments=
    Allows describing `<instrVoice>` instruments in more detail. Adds some playing technique marking elements.
=lutetab=
    Allows marking up of lute tablatures.

## Using Roma with the ODDs

The customisations are contained in two ODD files (plus one container
ODD file that pulls in all of MEI plus the two new modules). In order
to compile these into a schema file (XSD, RNG, etc.) you need to use
the 7.17.0 release (or later) of the
[TEI stylesheets](https://github.com/TEIC/Stylesheets). The build
process goes something like:

    $ git clone https://github.com/TEIC/Roma.git
    $ ln -s Roma/roma2.sh /path/to/bin/roma   # e.g. /usr/local/bin
    $ git clone https://github.com/TEIC/Stylesheets.git tei-xsl
    $ cd tei-xsl && make
    $ svn co http://music-encoding.googlecode.com/svn/trunk mei
    $ roma --xsl=/path/to/tei-xsl/ --localsource=/path/to/mei/source/driver.xml /absoluate/path/to/mei-tmus/schemata/mei-lutelab.odd
