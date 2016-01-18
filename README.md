# hp-41_period
## HP-41: The periodic table chemical elements for the HP-41 with much details.

This is a set of 3 4K HEPAX RAM pages. You can load these pages into an HP-41CL, an HP-41 with a NoV module or any other setup where you have a HEPAX module loaded and the ability to load HEPAX RAM pages. This means that HEPAX is a prerequisite for using the PERIOD program.

The HEPAX pages are configured with XROM numbers 18, 19 and 20.

The pages contain two programs, "PERIOD" and "NM".

"PERIOD" is the main program that will display lots of details of the 118 discovered chemical elements. The program relies on 4 big ASCII files included in the HEPAX pages, "ELEMENT", "ELEMNT2", "ELEMNT3" and "ELEMNT4". 

### PERIOD

Upon XEQ "PERIOD", you will be presented with a menu.

The program shows the short form of labels A-D:

**__0 N SY G↑P__**

Label (menu)	|Description
----------------|-----------
LBL A (0) |Input the atomic number in X and press "A" to show details for that element
LBL B (N) |Input (parts of) an element's name in Alpha to show details for that element
LBL C (SY) |Input an element's symbol in Alpha  to show details for that element
LBL D (G↑P) |Input Group number, ENTER↑, Period number to show details for that element
LBL e |Takes you back to the menu

The details for each element is:

* Atomic number, Name and Symbol
* Group, Period and Block
* Atomic Weight
* Property (Alkali metal, Noble Gas, etc.)
* Type (Gas, Liquid, Solid or Unknown)
* Occurrence in nature (Primordial, From Decay, Synthetic)
* Melting Point, Boiling Point (in Kelvin)
* Year of discovery ("OLD" if known in ancient times)
* Electron Configuration
* Atomic Radius (empirical and calculated)
* Origin (Big Bang, Cosmic Rays, Small & Large Stars, Large Stars, Large Stars & Super Nova, Super Nova and Man Made)

After showing all the detail for one lement in the sequence listed above, the program will show the details for the next element until it wraps around from 118 back to Hydrogen.

When showing the Group, Period, Block, the Y register will contain the Group number and the X register will contain the Period number. By adding 1 to X and pressing "D", you will jump one period down and show the element just below the current element. By subtracting 1 from X, you will jump to the element jut above it.

### NM (Nuclear Mass)

The program "NM" is included mostly because there was more space available. It is taken from the User Library Solutions, "Chemical Engineering" and calculates for a given element with a given number of protons (Z) and neutrons (N): Binding Energy, the Binding Energy per Nucleon, Mass of the Nucleus, Mass per Nucleon, Mass Excess of the Nucleus, Mass Excess per Nucleon, Volume Energy, Volume Energy per Nucleon, Surface Energy, Surface Energy per Nucleon, Coulomb Energy, Couloumb Energy per Nucleon, Symmetry Energy, Symmetry Energy per Nucleon, Pairing Energy and Pairing Energy per Nucleon. The details and listing of "NM" is given in "NuclearMass_NM.pdf".

