# QuPath_to_LCM
Galaxy workflow for converting QuPath annotations into laser capture microdissection coordinates from Zeiss devises. 

## Overview  
This repository provides a Galaxy workflow to connect [QuPath](https://qupath.github.io/) (for digital pathology annotation) with laser capture microdissection (LCM) systems from Zeiss.  

## Full Workflow  
The diagram below shows the overall experimental workflow:  

![Wet-lab + Computational Workflow](Overview_Workflow_QuPath_LCM.png)  

## Galaxy Workflow  
The individual steps of the Galaxy workflow are illustrated here:  

![Galaxy Workflow Steps](Overview_Galaxy_Workflow.png)  

- The workflow file (`QuPath_to_LCM_Galaxy_Workflow.ga`) is included in this repository and can be uploaded into any Galaxy instance.
- For convenience, you can also access it directly via this [Galaxy Workflow link](https://usegalaxy.eu/u/melanie-foell/w/qupath-to-lmd-workflow-direct-teachmark-file-import-and-using-collections).  

### Running the Workflow  
1. Log in to your Galaxy instance.  
   - Don’t have one? You can [register for free at usegalaxy.eu](https://usegalaxy.eu).  
2. Import the workflow:  
   - Either upload the `QuPath_to_LCM_Galaxy_Workflow.ga` file from this repository.  
   - Or import it directly using the shared Galaxy link above.  
3. Inputs for the workflow:
  - x and y coordinates as 2 column tabular file with a header line x and y containing at least three teachmark coordinates in QuPath
  - x and y coordinates as 2 column tabular file with a header line x and y containing at least three teachmark coordinates from physical slide in LCM device, the teachmarks have to be in the same order as in the first file
  - QuPath annotations as GeoJSON file
5. Run the workflow to generate a text file containing the annotations as txt file, that can directly be uploaded into Zeiss PALM RoboSoftware. An additional scatterplot showing the coordinates of the annotations is generated for visual control. 

## Citation  
If you use this workflow in your research, please cite this repository, a preprint manuscript will follow soon. 
