# Arbalet LAVA CAD files
## Requires FreeCAD 0.16
This variant is modeled thanks to [FreeCAD software](http://freecadweb.org/). As of February, 2016, the last stable version is FreeCAD 0.15.
However, these files use a new "expressions" feature available from 0.16. This feature allow to parameter datums and vary the thickness of materials. See http://www.freecadweb.org/wiki/index.php?title=Expressions 

To install the last development version on Ubuntu: 
http://freecadweb.org/wiki/?title=Download#Ubuntu_PPA_packages



## Assemblies require the Assembly 2 plug-in

Please install the [Assembly 2 plugin](https://github.com/hamish2014/FreeCAD_assembly2#freecad_assembly2) to be able to load assemblies and constraints.
It is not necessary to regenerate parts individually unless you need pictures of assemblies, but its overlap checking feature are very useful to check for defects.

## How to change parameters:

By changing any of these parameters FreeCAD will compute the other parameters.

Parameters:

* Thickness of the external wood: bottom#Slab.Height
* Thickness of the wood of the grid: strip_500#Strip.Width
* Thickness of the glass: glass#Glass.Height (Do not neglect, the rim of its host is based on that)

However, parts are not individually updated when a parameter changes in another file, execute the [ForceRecompute macro](http://www.freecadweb.org/wiki/index.php?title=Macro_ForceRecompute) in cascade for individual parts and then click on the "Update parts imported into the assembly" buttons for the assemblies.

## Notes
As of Feb, 2016, intervals of arrays have no units, thus in `(1000mm/3 + Slab.Height)/1mm` the last `/1mm` is only used to simplify the units of the result.
