# Pelagic-mizer-model
This repo contains the code for updating the pelagic mizer model for the Pacific
Islands region, including both the work that when into updating it and the files
for the corresponding [GitHub page](https://noaa-pifsc.github.io/Pelagic-mizer-model/).

## What's here
There are three groups of files in this repository: files to run the updated 
Pacific Islands region mizer model, files that went into updating this model, and
files for the cooresponding [GitHub page](https://noaa-pifsc.github.io/Pelagic-mizer-model/).

### Files to run mizer
This repository includes the species and fishing parameters needed to run the 
updated Pacific Islands region mizer model:  

* [Pelagic_params.csv](https://github.com/noaa-pifsc/Pelagic-mizer-model/blob/main/Pelagic_params.csv):
species parameters  
* [Pelagic_interaction.csv](https://github.com/noaa-pifsc/Pelagic-mizer-model/blob/main/Pelagic_interaction.csv):
interaction matrix  
* [Pelagic_gear_params_25_1.csv](https://github.com/noaa-pifsc/Pelagic-mizer-model/blob/main/Pelagic_gear_params_25_1.csv):
fishing gear parameters  
 
You can find references for the above parameters in 
[Pelagic_params_refs.csv](https://github.com/noaa-pifsc/Pelagic-mizer-model/blob/main/Pelagic_params_refs.csv).
  
To force your mizer simulations with modeled or empirical plankton data, as 
described in the model overview, use the files in 
[LinkingEnvironmentalData](https://github.com/noaa-pifsc/Pelagic-mizer-model/tree/main/LinkingEnvironmentalData). 
There's one for using satellite data and one for using earth system model (ESM)
output.

### Files to update the model
The files used to create those listed in the previous section, plus some 
some additional background work are in the [ModelBuild](https://github.com/noaa-pifsc/Pelagic-mizer-model/tree/main/ModelBuild)
folder.  

If you want to create your own parameter files, 
[Build_species_params.Rmd](https://github.com/noaa-pifsc/Pelagic-mizer-model/blob/main/ModelBuild/Build_species_params.Rmd)
is a tool to do that, although simply using your spreadsheet editor of choice is
probably more straightforward.  To create your own interaction matrix, use
[Build_interaction_matrix.Rmd](https://github.com/noaa-pifsc/Pelagic-mizer-model/blob/main/ModelBuild/Build_interaction_matrix.Rmd).

The [OceanographicData](https://github.com/noaa-pifsc/Pelagic-mizer-model/tree/main/ModelBuild/OceanographicData)
folder includes a [script](https://github.com/noaa-pifsc/Pelagic-mizer-model/blob/main/ModelBuild/OceanographicData/Domain_Oceanographic.Rmd)
we used to explore various oceanographic domains and create the base version of
the map in the GitHub page providing the model overview.  The 
[DietData](https://github.com/noaa-pifsc/Pelagic-mizer-model/tree/main/ModelBuild/DietData)
folders includes scripts used to work with the [Barnes et al. (2008)](https://doi.org/10.1890/07-1551.1)
diet data and the additional diet data used for albacore tuna.  It also includes
a script one could use if they were to add a micronekton group to the model.  The
[FisheryData](https://github.com/noaa-pifsc/Pelagic-mizer-model/tree/main/ModelBuild/FisheryData)
folder includes scripts to access and combine regional observer data and to 
map international effort data.  There are also scripts to examine and then map
fishery characteristics.  This folder also includes the scripts used to create
catch spectra from observer data and to compare modeled and observed catch.

### Files for the model overview
This repo also includes files for the GitHub page that provides the model 
overview.  These files end in .qmd, .yml, .csl, and .bib.  They also live in 
the folders not discussed above.  In general, if you're simply interested in 
running mizer as described in the model overview, you can ignore these files.

---

### Disclaimer

This repository is a scientific product and is not official communication of the 
National Oceanic and Atmospheric Administration, or the United States Department 
of Commerce. All NOAA GitHub project content is provided on an 'as is' basis and 
the user assumes responsibility for its use. Any claims against the Department 
of Commerce or Department of Commerce bureaus stemming from the use of this 
GitHub project will be governed by all applicable Federal law. Any reference to 
specific commercial products, processes, or services by service mark, trademark, 
manufacturer, or otherwise, does not constitute or imply their endorsement, 
recommendation or favoring by the Department of Commerce. The Department of 
Commerce seal and logo, or the seal and logo of a DOC bureau, shall not be used 
in any manner to imply endorsement of any commercial product or activity by DOC 
or the United States Government.

### License
This repository uses the Apache 2.0 license. 
Additionally, software code created by U.S. Government employees 
is not subject to copyright in the United States (17 U.S.C. §105). 
The United States/Department of Commerce reserves all rights to 
seek and obtain copyright protection in countries other than the 
United States for Software authored in its entirety by the Department 
of Commerce. To this end, the Department of Commerce hereby grants 
to Recipient a royalty-free, nonexclusive license to use, copy, and 
create derivative works of the Software outside of the United States.
See LICENSE for further details.