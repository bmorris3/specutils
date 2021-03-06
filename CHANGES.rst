1.1
---

New Features
^^^^^^^^^^^^

Bug Fixes
^^^^^^^^^

- Fixed ``tabular-fits`` handling of 1D+2D spectra without WCS;
  identification and parsing of metadata and units for ``apogee``
  and ``muscles`` improved; enabled loading from file-like objects. [#573]

Other Changes and Additions
^^^^^^^^^^^^^^^^^^^^^^^^^^^


1.0
---

New Features
^^^^^^^^^^^^

- Implement ``SpectralCoord`` object. [#524] 

- Implement cross-correlation for finding redshift/radial velocity. [#544]

- Improve FITS file identification in default_loaders. [#545]

- Support ``len()`` for ``SpectrumCollection`` objects. [#575]

- Improved 1D JWST loader and allow parsing into an ``SpectrumCollection`` object. [#579]

- Implemented 2D and 3D data loaders for JWST products. [#595] 

- Include documentation on how to use dust_extinction in specutils. [#594]

- Include example of spectrum shifting in docs. [#600]

- Add new default excise_regions exciser function and improve subregion handling. [#609]

- Implement use of ``SpectralCoord`` in ``Spectrum1D`` objects. [#610]

Bug Fixes
^^^^^^^^^

- Fix stacking and unit treatment in ``SpectrumCollection.from_spectra``. [#578]

- Fix spectral axis unit retrieval. [#581]

- Fix bug in subspectrum fitting. [#586] 

- Fix uncertainty to weight conversion to match astropy assumptions. [#594]

- Fix warnings and log messages from ASDF serialization tests. [#597]

Other Changes and Additions
^^^^^^^^^^^^^^^^^^^^^^^^^^^

- Remove spectral_resolution stub from Spectrum1D. [#606]


0.7
---

New Features
^^^^^^^^^^^^

- Make specutils compatible with Astropy 4.0 (breaking change). [#462]

- Remove all wcs adapter code and rely on APE14 implementation. [#462]

Bug Fixes
^^^^^^^^^

- Address ``MexicanHat1D`` name change in documentation. [#564]


0.6.1
-----

API Changes
^^^^^^^^^^^

- Resamplers now include ``extrapolation_treatment`` argument. [#537]

- Template fitting now returns an array of chi squared values for each template. [#551]

New Features
^^^^^^^^^^^^

- Masks now supported in fitting operations. [#519]

- Resamplers now support resamping beyond the edge of a spectrum using. [#537]

- New template fitting for redshift finding. [#527]

- New continuum checker to discern whether continuum is normalized or subtracted. [#538]

- Include documentation on how to achieve splicing using specutils. [#536]

- Include function to calculate masks based on S/N thresholding. [#509]

Bug Fixes
^^^^^^^^^

- Include new regions regression tests. [#345]

- Fix fitting documentation code block test. [#478]

- Fix Apogee loader to incorporate spectral axis keyword argument. [#560]

- Fix tabular fits writer and include new regression test. [#539]

- Fix dispersion attribute bug in ``Spectrum1D`` objects. [#530]

- Correctly label regression tests that require remote data. [#525]

Other Changes and Additions
^^^^^^^^^^^^^^^^^^^^^^^^^^^

- Switch to using ``gaussian_sigma_width`` for ``Gaussian1D`` fitting estimator. [#434]

- Update documentation side bar to include page listing. [#556]

- New documentation on ``spectrum_mixin``. [#532]

- Model names are now preserved in the ``fit_lines`` operation. [#526]

- Clearer error messages for incompatible units in line fitting. [#520]

- Include travis stages in test matrix. [#515]


0.6
---

New Features
^^^^^^^^^^^^

- New redshift and radial velocity storage on `Spectrum1D` object.

- Spectral template matching including resampling.

- Error propagation in convolution smoothing.

- Sub-pixel precision for fwhm calculations.

- New spectral resampling functions.

- New IRAF data loaders.

- New FWZI calculation.

Bug Fixes
^^^^^^^^^

- Stricter intiailizer for ``Spectrum1D``.

- Correct handling of weights in line fitting.

- Array size checking in `Spectrum1D` objects.

- Fix for continuum fitting on pixel-axis dispersions.

Other Changes and Additions
^^^^^^^^^^^^^^^^^^^^^^^^^^^

0.5.3
-----

Bug Fixes
^^^^^^^^^

- Fix comparison of FITSWCS objects in arithmetic operations.

- Fix example documentation when run in python interpreter.


0.5.2 (2019-02-06)
----------------

Bug Fixes
^^^^^^^^^
- Bugfixes for astropy helpers, pep8 syntax checking, and plotting in docs [#416,#417,#419]

- All automatically generated ``SpectrumList`` loaders now have identifiers. [#440]

- ``SpectralRange.from_center`` parameters corrected after change to SpectralRange interface. [#433]

Other Changes and Additions
^^^^^^^^^^^^^^^^^^^^^^^^^^^
- Improve explanation on creating spectrum continua. [#420]

- Wrap IO identifier functions to ensure they always return True or False and log any errors. [#404]


0.5.1 (2018-11-29)
------------------

Bug Fixes
^^^^^^^^^

- Fixed a bug in using spectral regions that have been inverted. [#403]

- Use the pytest-remotedata plugin to control tests that require access to remote data. [#401,#408]


0.5 (2018-11-21)
----------------

This was the first release of specutils executing the
[APE14](https://github.com/astropy/astropy-APEs/blob/master/APE14.rst)
plan (i.e. the "new" specutils) and therefore intended for broad use.
