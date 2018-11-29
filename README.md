# WF-1-WF
![myimage-alt-tag](https://github.com/WF-ShAre/WF-1-WF/blob/master/WF-1.jpg)


  WF-Title: WF-1
  version: 1.0
  Description: The workflow performs some basic execution extracted from NJ-WF 

###WF-Tasks:

  No-of-tasks: 7
  Tasks: {importFile: 1, filterDuplicate: 1, clustalw: 1, Mega-NJ: 1, zipfile: 1, exportFile: 2}
  Dependency-Libs: {java1.7: all, clustalw-lib: clustalw, wine1.6: Mega-NJ, Mega-CC: Mega-NJ} 

###Blueprint:

  blueprint-name: WF-1.yaml
  Docker-images: 
  sizes: 563 MB (Virtual size 1.421 GB)
  OS-types: ubuntu14.4
  tools: 

###Input:

  input-file: {'file1'}
  description: A file for importfile task
  types: 


###Execution-Environment:

  Cloudify-version: 3.2
  Docker-version: 1.8+
  OS-type: ubuntu14.04
  Disk-space: 10 GB
  RAM: 3 GB

#Deployment Instruction
This repository includes all files and scripts to deploy WF-1 workflow on Multiple Docker containers as follow:

1- Clone the repository to your machine with --recursive option, open a terminal window and change to workflow repository.  
2- To execute the workflow and the attached input sample, in the terminal run:   
   . ./WF-1-deploy.sh 1    
3- If you have own input files, copy your files to WF-1/Input-sample folder, open Input.yaml file and change input files name, then
   run:  
   . ./WF-1-deploy.sh 1   
    
After successfully running the workflow, five output files can be found in ~/WF-1 folder
