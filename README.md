# JKBio

A list of awesome functions for every Computational Biologist


## Content

### Terra

_in ./TerraFunction.py_

a file containing a set of functions that uses [dalmatian]() to interact with the [GCP]() powered genomics HPC platform: [Terra](). 
They contain a list of additional functions to do more than what is available in dalmatian

#### Available functions:


- createManySubmissions: 
- waitForSubmission: 
- uploadFromFolder: 
- updateAllSampleSet: 
- addToSampleSet: 
- addToPairSet: 
- changeGSlocation: 
- renametsvs: 
- findBackErasedDuplicaBamteFromTerraBucket: 
- shareTerraBams: 
- saveConfigs: 
- cleanWorkspace: 
- saveOmicsOutput: 
- shareCCLEbams: 

### epigenomics/ChipHelper

ChipHelper is especially targeted to functions related to the analysis of epigenomics data. It has functions to read, merge, denoise, ChIP seq data, it contains a lot of functions required for the AML paper.

#### Available functions:


- dropWeirdChromosomes: 
- extractPairedSingleEndFrom: 
- findReplicates: 
- computeSingleEnd: 
- computePairedEnd: 
- bigWigFrom: 
- mergeBams: 
- loadPeaks: 
- pysam_computePeaksAt: 
- bedtools_computePeaksAt: 
- computePeaksAt: 
- simpleMergedPeaks: 
- findpeakpath: 
- mergeReplicatePeaks: 
- findAdditionalPeaks: 
- putInConscensus: 
- findAdditionalCobindingSignal: 
- fullDiffPeak: 
- diffPeak: 


### Helper

_in ./Helper.py_

a set of plotting tools based on [matplotlib]() and [bokeh]() and additional helper functions to save data, do merging of dataframes, etc.. 
It mostly contains a list of early function that will then be respectively integrated.

#### Available functions:


- fileToList: convert a txt with a list of values to a python list
- listToFile: converts a list of values to a txt
- dictToFile: converts a dict to a json
- fileToDict: converts a json to a dict
- batchMove: move a lot of file in batch (can provide different locations)
- batchRename: rename a bunch of files in batch
- filterProteinCoding: removes all non protein coding genes from a list (you need taiga access)
- convertGenes: converts genes from a naming to another (you need taiga access)
- scatter: makes a hoverable/zoomable bokeh scatter plot
- CNV_Map: makes a hoverable Copy Number plot using bokeh
- volcano: makes a searchable volcano plot for a Differential expression experiment using bokeh
- plotCorrelationMatrix: makes a hoverable bokeh correlation matrix
- venn: makes a venn diagram from a list of sets
- grouped: to use in a forloop to group values in batch
- mergeImages: merge multiple pngs/pdfs together into one
- addTextToImage adds a text in an image to a specific location
- overlap: given two tuples, returns the overlap
- union: given two tuples, returns the union
- nans: gets nans from a panda df
- createFoldersFor: makes the required folders for a given filepath
- randomString: generate a random string for namings
- parrun: runs list of commands in parallel
- askif: ask the user a questions and returns the y/n answer
- inttodate: converts an int to a string date.
- datetoint: converts a date to an int
- getBamDate: get the date of creation of a bam file
- getSpikeInControlScales: extracts the spike in control values from a set of bam files
- changeToBucket: move values to a bucket
- GSEAonExperiments: perform GSEA to compare a bunch of conditions at once
- runERCC: creates an ERCC dashboard and extract the RNA spike ins from it (need rpy2 and ipython and R's ERCCdashboard installed)


### GCP

_in ./GCPFunctions.py_

#### Available functions:

- mvFiles: move a set of files in parallel (when the set is huge)
- lsFiles: list a set of files in parallel (when the set is huge)
- cpFiles: copy a set of files in parallel (when the set is huge)
- catFiles: copy a set of files in parallel (when the set is huge)
- rmFiles: remove a set of files in parallel (when the set is huge)
- recoverFiles: moves back delete files (saved with versionning) in parallel (when the set is huge)
- patternRN: rename a bunch of files in parallel
- get_all_sizes: will sort and list all the files by their sizes. 
- exists: tells if a gcp path exists
- extractSize: extract the size from the string returned by an ls -l|a command
- extractPath: extract the path from the string returned by an ls -l|a command
- extractHash:  extract the crc32 from the string returned by an ls -L command


### pyDEseq2

_in ./helper/pyDESeq2.py_

it is a python integration of [deseq2]() (the differential expression analyser) with [rpy2]()


### Datanalytic

a set of function to do better data analytics (supplement of numpy, pandas etc..)


### taigr

a version of taiga that do not requires RCurl (and can save you when you have a faulty RCurl-Curl link)


### data

should not contain anything when pulled but is used by any of the functions in the folder, to save some required data files


### cell_line_mapping

a set of functions to map cell line ids to other cell line ids based on an up to date google spreadsheet. 


you can import files in python with e.g. `from JKBio import TerraFunction as terra`


### Bash Functions:

- update_my_playlists
- convert2gif
- launchandco
- retrieve_remote_file_size
- removeFirstLineOf
- upload_urls_to_gcp
- gitpush
- create_dx_urls_from
- get_unuploadedfiles_from_dx_to_gcp
- continue_upload

- rename_bunch
- extract
- myinfo: prints my info (only on mac)
- kp: kill process 
- ssd: get ssd info (only on mac)


## Reason

As I am working in different domains of computational genomics, I need to have a set of reusable function that will help me during my work.
It can be functions to work with different tools that I have to use. Functions to do some plots. etc..

I will be trying to keep each of these functions functional and documented. Feel free to pull and start use anything that might be useful to you.
If you see anything suspicious or not working. A pull request would definitely get reviewed within a day.

I hope to be able to give back to the community and maybe save a couple of hours to couple of researchers.

Best.

#/!\ Under construction /!\

jkalfon@broadinstitute.org

jkobject@gmail.com

https://jkobject.com

Apache license 2.0.