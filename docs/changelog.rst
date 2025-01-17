Changelog
=========

1.1.0 (unreleased)
^^^^^^^^^^^^^^^^^^

* Extrapolation of NenuFAR antenna model (:func:`~nenupy.instru.instru.nenufar_ant_gain`) above 80 MHz [`#22 <https://github.com/AlanLoh/nenupy/issues/22>`_].
* Implementation of :class:`~nenupy.observation.tapdatabase.ObsDatabase` class, which enables queries over the NenuFAR BST database in order to seach for particular past observations within a given :attr:`~nenupy.observation.tapdatabase.ObsDatabase.time_range` and/or :attr:`~nenupy.observation.tapdatabase.ObsDatabase.freq_range` and/or around a given sky position :attr:`~nenupy.observation.tapdatabase.ObsDatabase.fov_center` with a given search radius :attr:`~nenupy.observation.tapdatabase.ObsDatabase.fov_radius`.
* Addition of a ``text`` option to :meth:`~nenupy.astro.hpxsky.HpxSky.plot` aiming at overplotting text (such as source names) at some given equatorial positions.
* UVW computation corrected (sign convention in order to call imaging TF as :math:`\int V e^{-2\pi i (ul + vm)}\, du\, dv`) [`#23 <https://github.com/AlanLoh/nenupy/issues/23>`_].
* NenuFAR data rate estimation implemented (:func:`~nenupy.instru.instru.data_rate`).
* Conversion between frequencies and subband indices :func:`~nenupy.instru.instru.freq2sb` and :func:`~nenupy.instru.instru.sb2freq`.
* Dispersion delay added (:func:`~nenupy.astro.astro.dispersion_delay`).
* Implementation of :class:`~nenupy.undysputed.dynspec.Dynspec` to read/de-disperse/rebin (in time and/or frequency) high-rate UnDySPuTeD time-frequency data (or `DynSpec data <https://nenufar.obs-nancay.fr/en/astronomer/#data-products>`_) [`#30 <https://github.com/AlanLoh/nenupy/issues/30>`_].
* Correct for 6 min jumps in Undysputed DynSpec data [`#32 <https://github.com/AlanLoh/nenupy/issues/32>`_].
* Implemented background computation for :class:`~nenupy.beamlet.sdata.SData` objects (:attr:`~nenupy.beamlet.sdata.SData.background` and :attr:`~nenupy.beamlet.sdata.SData.fbackground`) as well as a plotting method :meth:`~nenupy.beamlet.sdata.SData.plot`.
* SQL database
* Add functions to get a source coordinates and compute the horizontal coordinates versus time (:func:`~nenupy.astro.astro.getSource` and :func:`~nenupy.astro.astro.altazProfile`).
* Plot of observation pointing files ``alatazA`` and ``altazB`` (:func:`~nenupy.observation.pointing.plotPointing`)
* Correction of bugs and improvement of the ``astro`` module [`#38 <https://github.com/AlanLoh/nenupy/issues/38>`_]
* Faster version of equatorial/horizontal coordinates conversion (:func:`~nenupy.astro.astro.toAltaz`)
* Addition of Earth coordinates converters (:mod:`~nenupy.astro.astro`)
 

1.0.0 (2020-04-29)
^^^^^^^^^^^^^^^^^^

Major refactoring of the original `nenupy` package.