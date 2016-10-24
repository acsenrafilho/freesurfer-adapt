# freesurfer-adapt
Simple script to add different brain extraction methods inside default FreeSurfer cortical reconstruction pipeline.


# Brief introduction

The ``recon-all-adapt`` script is intended to use different brain extraction methods in FreeSurfer cortical reconstruction pipeline, which has been reported as an important step for obtaining more accurate cortical surface estimates.

The brain extraction methods available to use are:
* [BET (FSL)](http://fsl.fmrib.ox.ac.uk/fsl/fslwiki/BET)
* [3dSkullStrip (AFNI)](https://afni.nimh.nih.gov/pub/dist/doc/program_help/3dSkullStrip.html)
* [optiBET](https://montilab.psych.ucla.edu/fmri-wiki/optibet/)
* [ROBEX](https://www.nitrc.org/projects/robex/)

More details could be found in recent publications ([abstract](),[paper]())

# How to use
* [Download](https://github.com/acsenrafilho/freesurfer-adapt/archive/master.zip) the freesurfer-adapt folder project
* Decompress the file in a desired folder location (for example, in /usr/local/freesurfer-adapt)
* Add the folder path in your system environment. One way to do that could be done with the follwing instructions:

```
gedit ~/.bashrc
```
Once opened the ``.bashrc`` file in gedit (text editor), you can insert the following lines:

```
PATH=$PATH:<path/to/user/freesurfer-adapt>
```
Note that the ``<path/to/user/freesurfer-adapt>`` represents the full path for the folder where you decompressed the downloaded file (in our example, /usr/local/freesurfer-adapt).

* Save the ``.bashrc`` file and open a new terminal

At this moment, with a new terminal opened, you could run the the script with the following command:

```
recon-all-adapt <path/to/T1.nii.gz> <Brain extraction method>
```
**NOTE:** The variables for each brain extraction method is given in the config_variables.conf file, located inside the ``freesurfer-adapt`` folder.

# Contact

If you need more details about this script, please feel free to send me an [email](mailto:acsenrafilho@gmail.com)
