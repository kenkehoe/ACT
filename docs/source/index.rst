.. toctree::
   :maxdepth: 2
   :hidden:
   :caption: Version 2 Release Guide

   userguide/GUIDE_V2.rst

.. toctree::
   :maxdepth: 2
   :hidden:
   :caption: User Guide

   userguide/index.rst

.. toctree::
   :maxdepth: 2
   :hidden:
   :caption: Reference Guide

   API/index.rst

.. toctree::
   :maxdepth: 2
   :hidden:
   :caption: Example Gallery

   source/auto_examples/index.rst

.. toctree::
   :maxdepth: 1
   :hidden:
   :caption: Blog

   blog.md

.. toctree::
   :maxdepth: 1
   :hidden:
   :caption: Getting Help

   GitHub Issue Tracker <https://github.com/ARM-DOE/ACT/issues>


Atmospheric Community Toolkit (ACT)
===================================
The Atmospheric data Community Toolkit (ACT) is an open source Python toolkit for working with atmospheric time-series datasets of varying dimensions.  The toolkit is meant to have functions for every part of the scientific process; discovery, IO, quality control, corrections, retrievals, visualization, and analysis.   It is meant to be a community platform for sharing code with the goal of reducing duplication of effort and better connecting the science community with programs such as the `Atmospheric Radiation Measurement (ARM) User Facility <http://www.arm.gov>`_.  Overarching development goals will be updated on a regular basis as part of the `Roadmap <https://github.com/AdamTheisen/ACT/blob/master/guides/ACT_Roadmap.pdf>`_  .

|act|

.. |act| image:: act_plots.png

Please report any issues or feature requests by submitting an `Issue <https://github.com/ARM-DOE/ACT/issues>`_.  Additionally, our `discussions boards <https://github.com/ARM-DOE/ACT/discussions>`_ are open for ideas, general discussions or questions, and show and tell!

ACT's Third Roadmap
===================

To meet the needs of the community and stakeholders, ACT will be creating a new roadmap.
This roadmap will continue a plan forward on features to improve on and to add in newer ACT
versions. A part of this new roadmap is a survey from the community that will provide feedback
for the developers on priorities for newer ACT versions. If time permitting, and you are a user of ACT
or are considering to use ACT the survey can be found here: `ACT Roadmap Survey <https://docs.google.com/forms/d/e/1FAIpQLScLQBH9ROP0sKMr_DvUnLKGT-K8pzc1b3zg21QqppNT_gTa2Q/viewform?usp=sf_link>`_
The feedback would be much appreciated.

Dependencies
============

| `xarray <https://xarray.pydata.org/en/stable/>`_
| `NumPy <https://www.numpy.org/>`_
| `SciPy <https://www.scipy.org/>`_
| `matplotlib <https://matplotlib.org/>`_
| `skyfield <https://rhodesmill.org/skyfield/>`_
| `pandas <https://pandas.pydata.org/>`_
| `dask <https://dask.org/>`_
| `Pint <https://pint.readthedocs.io/en/0.9/>`_
| `PyProj <https://pyproj4.github.io/pyproj/stable/>`_
| `Proj <https://proj.org/>`_
| `Six <https://pypi.org/project/six/>`_
| `Requests <https://2.python-requests.org/en/master/>`_
| `MetPy <https://unidata.github.io/MetPy/latest/index.html>`_

Optional Dependencies
=====================

| `MPL2NC <https://github.com/peterkuma/mpl2nc>`_ Reading binary MPL data.
| `Cartopy <https://scitools.org.uk/cartopy/docs/latest/>`_ Mapping and geoplots
| `Py-ART <https://arm-doe.github.io/pyart/>`_ Reading radar files, plotting and corrections
| `scikit-posthocs <https://scikit-posthocs.readthedocs.io/en/latest/>`_ Using interquartile range or generalized Extreme Studentized Deviate quality control tests
| `icartt <https://mbees.med.uni-augsburg.de/docs/icartt/2.0.0/>`_ icartt is an ICARTT file format reader and writer for Python


Contributing
============

ACT is an open source, community software project. Contributions to the
package are welcomed from all users.

The latest source code can be obtained with the command::

    git clone https://github.com/ARM-DOE/ACT.git

If you are planning on making changes that you would like included in ACT,
forking the repository is highly recommended.

We welcome contributions for all uses of ACT, provided the code can be
distributed under the BSD 3-clause license. For more on
contributing, see the `contributor's guide. <https://arm-doe.github.io/ACT/CONTRIBUTING.html>`_

Testing
=======

For testing, we use pytest for running the unit tests and arm-test-data for
test files that are used for the unit tests. To install pytest::

   $ conda install -c conda-forge pytest

And for matplotlib image testing with pytest::

   $ conda install -c conda-forge pytest-mpl

To install arm-test-data::

   $ conda install -c conda-forge arm-test-data

After installation of both pytest and arm-test-data, you can launch the test
suite from outside the source directory (you will need to have pytest
installed and for the mpl argument need pytest-mpl)::

   $ pytest --mpl --pyargs act

In-place installs can be tested using the `pytest` command from within
the source directory.
