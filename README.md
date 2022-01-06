# ICSL KiCad Library
This is the repository for KiCad Library used in ICSL projects. The library only works for KiCad Version 6+.

- `ICSL.kicad_sym`: symbol library file
- `ICSL.lib`: old KiCad version 5 library (archived as of 1/6/2022)
- `ICSL.pretty`: footprint library folder
- `prj-kicad-jlcpcb`: submodule of [prj-kicad-jlcpcb](https://github.com/TomKeddie/prj-kicad-jlcpcb.git)


### Setting up
First, make sure you are running KiCad version 6+. Clone this repository with submodules:
```bash
git clone --recurse-submodules -j8 https://github.com/Columbia-ICSL/kicad-library.git
```

Open KiCad. Go to preferences - configure paths, click on the "+" sign and add an entry with Name: `ICSL_LIB`, Path: `path/to/this/repo`. Click "OK" to save.

Go to preferenes - manage symbol libraries - global libraries. Click on the folder icon next to "+", and select the `ICSL.kicad_sym` file.
Click on the folder icon again and select all `.lib` files in the `prj-kicad-jlcpcb/libraries` folder.

Go to preferences - manage footprint libraries - global libraries. Click on the folder icon next to "+", and select the `ICSL.pretty` folder.

To check the libraries are imported correctly, open "Symbol Editor" and verify that "ICSL", "jlcpcb-basic-XXX" libraries are on the list. Open "Footprint Editor" and verify that "ICSL" is on the list. Click on ICSL > Amphenol_91911-31321LF_PLUG and go to View - 3D Viewer to confirm that the 3D model renders correctly.
