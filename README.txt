The materials in this repo supplement the article, "A Demonstration of
Interstellar Navigation Using New Horizons," by Lauer, Munro, Spencer, et.al.,
accepted for publication in The Astrophysical Journal 2025,

nhparallax.ipynb
    is a Jupyter notebook containing the details of our calculations of all or
    nearly all of the numbers presented in the Tables and text of the article,
    showing in detail how we arrived at them.  In particular, the navigation
    equations presented in section 3 are implemented in scipy code.  The
    matplotlib code used to produce Figures 3 and 4 of the paper is also here.
    While we have added extensive comments both in the code and in display
    cells of the notebook, this material has not been reviewed with anything
    close to the level of care of the paper itself - the comments are not
    perfectly consistent with the text of the article, and in any cases of
    disagreement or ambiguity, the article is authoritative.  (The numerical
    and plotted results, on the other hand, should correspond precisely with
    the article.)

nhjpl_traj.txt
    is output from JPL Horizons at https://ssd.jpl.nasa.gov/horizons/app.html#/
    The output contains not only the trajectory of the New Horizons spacecraft
    for the first 15 years of its journey (as plotted in Figure 3 and 4), but
    also detailed explanations of the precise meaning of the data, with
    enough information that a student could reconstruct the query that led to
    this file.

nearby100.txt
    Basic data on the nearest 100 stars obtqained from Simbad using the query
    mentioned in the file.  See https://simbad.u-strasbg.fr/simbad/ for more
    information.  Only a few rows are used in the article, mostly to construct
    Table 4, but a student could use more in conjunction with the ramk_pairs
    and rank_triples to explore some of the claims about optimal choices of
    sets of stars for use as navigational landmarks.

The nhparallax.ipynb file includes functions for querying the Gaia archive
which are partially commented out (that is, the python import statements
required to load their dependencies are commented out).  However, instead of
invokijng these functions to retrieve the Gaia archive data, the notebook
contains the results of these queries as simmply data loads.  Similarly, all
of the image analysis results are merely loaded as data.  A variety of image
processing software was used to generate these results - namely the positions
of the target stars relative to other known stars in the images - but none of
this software is described or included here.  The comments cite the author and
date these analyses were carried out, but no more details.

We provide an MIT license for the contents of this repo for purposes of clarity.
Anyone is free to use either the code or the data however they wish.  This is
by no means intended to be a finished software product; it has undergone
minimal testing, and has been checked only for the specific cases described in
the article.  We do not anticipate maintaining this code in any way; it merely
serves as a record of how we arrived at the numbers used in the article.

The software required to run the notebook consists of jupyter, ipython with its
standard libraries including numpy, scipy, and matplotlib as obtained from
https://www.anaconda.com/download in November of 2024, based on python 3.12.2.
