# Thin Film Diagnosis using Hyperspectral imaging

This repository contains all the source files that are analysed using 'HyperSpectral Image Analysis.ipynb'


The types of data files in this repository are '.bil', '.bil.hdr' and '.txt' files.
The '.bil' and '.bil.hdr' file extensions are the Hyperspectral image and its corresponding header.
Both files are required to parse the hyperspectral images using the Jupyter notebook. 

The files follow the following naming convention "HSI-{Solvent}-{Concentration}mM.bil" and the same convention for the header files ('.bil.hdr').
All samples are P3HT thin films doped with F4TCNQ with the concentration levels indicated on the file name.


The files ending with '.txt' is the data from the UV-VIS spectrometer for each sample.
They follow the naming convention of '{solvent}_UV_VIS_{concentration}mM.txt'.


To use the Hyperspectral image files in the jupyter notebook, the function read_bil() is used with the file location of the .bil file as the input parameter.
The header file must be in the same location as the .bil file for the function to run without error.

The ideal filesystem for the code to run without many changes would be a folder containing all the .bil and .bil.hdr files for a particular solvent, and parent folder containing each solvent's folder.

For example : Let 'images/' be a parent folder. Under 'images/' there will be 5 folders , one for each solvent, and in each of those folders would be the hyperspectral image files for that particular solvent.

To run the file you wil also need 'bands.csv' and 'labels.txt' as they provide information for plotting and are essential to automating the program.
