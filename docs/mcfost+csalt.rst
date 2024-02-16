MCFOST + csalt
==============

Converting an MCFOST model to a synthetic MS file (via csalt)
-------------------------------------------------------------

You can convert an MCFOST model to a synthetic MS (measurement set) file by overwriting the visibilities in a pre-existing MS file. We make use of several functions provided in `csalt <https://github.com/seanandrews/csalt>`__ to do this. To run the following you need to have modular casa installed so you can use the casatools python library, as well as all the dependencies in csalt which includes the `vis_sample <https://github.com/AstroChem/vis_sample>`__ package. Currently the MCFOST interface is only implemented in `Caitlyn Hardiman's branch of csalt <https://github.com/caitlynhardiman/csalt>`__, aiming to merge with the main branch very soon.


You will need to define the following variables:

- data = the MS file you are using as your template ('input.ms')
- filename = the path to your MCFOST model's data_CO folder ('model/data_CO')
- outfile = the name of your output synthetic MS file ('output.ms')

You also need to ensure that the velocity range/spacing and the emission line you have used in your model match those of the MS file you are using as a template. You can then generate the synthetic MS file using the following code:

::

     from csalt.helpers import *
     from csalt.model import *

     data_dict = read_MS(data)
     cm = model(‘MCFOST’)
     model_dict = cm.modeldict(data_dict, {data: filename})
     write_MS(model_dict, outfile=outfile)
