# Introduction
This repo contains the 3D printed parts and printing instructions for a Big Red^H^H^HRound Button, part of the front garden railway project.  For assembly instructions see here:

https://www.meades.org/misc/big_round_button/big_round_button.html

For more general information on the front garden railway see here:

https://www.meades.org/railways/garden/garden.html

The main file is `big_round_button.blend`, the components of which are exported to a number of `big_round_button*.stl` files at a Blender scale factor of 1000 to give real size in millimetres. `_xY` on the end of an `stl` file name means you will need to print `Y` of those parts (e.g. 8 of `big_round_button_spring_support_x8.stl`).

# Printing
## `big_round_button_button.stl`
The chief challenge with this print is getting the button to come out as transparent as possible.  For my [Prusa MK4S](https://www.prusa3d.com/product/original-prusa-mk4s-3d-printer-5/) filament printer I took the PrusaSlicer generic PETG settings and, based on the advice [here](https://forum.prusa3d.com/forum/original-prusa-i3-mk3s-mk3-how-do-i-print-this-printing-help/transparent-petg/) and [here](https://www.printables.com/model/15310-how-to-print-glass), made the following modifications:

- set 100% in-fill: a solid mass of plastic,
- set the maximum print speed for all types of print to 20&nbsp;mm/s: nice and slow,
- reduced the cooling fan to between 10% and 15%,
- increase the temperature to 250&nbsp;C to ensure melding of adjacent layers,
- set the layer height to 0.1&nbsp;mm (greatest detail, packing more filament in),
- increase the filament flow rate to 5% greater than normal; this will compress the layers nice and hard,
- set the fill type and the support interface layer type to concentric: this should match the shape of the button,
- set the in-fill angle to 0 degrees; this should make the outer layers print as a horizontal/vertical grid,
- enabled a safety feature in the slicer program to not have the nozzle cross perimeters, reducing the changes of it hitting anything.

Then I printed the button (`big_round_button_button.stl`) in SUNLU transparent white PETG, supports required on the build plate.  The print will probably take around 2 or 3 days with these settings.

Note that PETG is not UV-safe, I don't believe there is a UV-safe transparent filament; the button will just need to be replaced every few years.

## Everything Else
Everything else should be printed in ASA (for UV-safety), likely black in colour, fastest speed, 15% in fill, no supports required.  You might wish to use a brim on `big_round_button_housing.stl` to ensure it stays attached to the build plate.