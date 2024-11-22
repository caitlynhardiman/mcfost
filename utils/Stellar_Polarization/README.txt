#From https://www.astro.umd.edu/~jph/MARCS_new/
#Files were corrected. I replaced _ by -

Polarization and limb darkening of plane-parallel atmospheres
of solar composition for 20 wavelengths between 2800A and 8000A.

These results were extracted from MARCS model atmospheres with
solar abundances and 1 km/sec microturbulence. The file name
is based on the temperature and log gravity: T3500g3.5 is a
model with Teff=3500K, log(g)=3.5. There is also a solar model,
indicated by T5777g4.44.

There are 65 rows in each file. The first row is the effective
temperature, log of the gavity, and metal abundance relative to
solar of the model. (We present models with Z=1, 1/10 & 1/100.)

The second row gives the values of the 20 continuum wavelengths.
The third row gives the emergent (astrophysical) flux F_nu  at
these 20 wavelengths.

The fourth row gives the 159 values of \mu (= cos \theta) at
which I(\mu) and Q(\mu) are tabulated, while the fifth row is
the corresponding angle \theta in degrees.

The remaining 60 rows are 20 groups of three: (1) the emergent
intensity I(\mu), (2) the Stokes paramenter Q(\mu), and (3) the
polarization Q(\mu)/I(\mu). Each row contains 159 values.
The first 3 rows are for the 1st wavelength, 8000A, the next
3 for 7500A, and so on until the last 3 rows for 2800A.

The polarization is highest for \mu near zero,i.e., for radiation
emerging nearly parallel to the surface of the stellar atmosphere,
varies rapidly as \mu goes to zero, so I have spaced the values
of \mu more closely there.

Note that the Stokes vector Q is measured with respect to the
vertical, so radiation near the limb (\mu small) is generally
negative, as the light is polarized parallel to the surface of
the atmosphere.
