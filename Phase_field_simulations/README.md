# README

## Requirements & Installation for Phase-field package

### TLDR Recipe (details below)

`conda create --name <MYFIPYENV> --channel conda-forge python=2.7 numpy scipy matplotlib pysparse mayavi weave`


`activate <MYFIPYENV>`

`pip install fipy`

`pip install moviepy` (This is for generating mp4 files)

`sudo apt-get install gifsicle` (This generates optimized GIF files)

`pip install imageio` (this is for unoptimized GIF files)

### Documentation

Navigate to **docs/build/html/index.html** and launch the file in browser to get user-friendly overview of the detailed documentation.

### Running the code

`python phase_field --i $input_file --o $output_folder --p $param_file`

$input_file contains the text-file with the input parameters (see Input/input_params.txt for reference) in the following format

`param,value \n`

$output_folder contains the path to output_folder which will be created as Output/output_folder

$param_file is an optional input file & it contains a list of parameters to iterate over in the following format (see Input/param_list.txt for reference):

`param`

`value1`

`value2`

Specifying --pN 2 while running the code with a param file will only execute the code with 2nd parameter value in list.
### To-do
1. Support for 3D plots & movies on cluster
2. Support for arbitrary choice of free-energy
3. Plotting summary statistics by default

### Long version
This code is written to employ the latest version of fipy (3.3.1) interfacing with py 2.7.15.

The [FiPy webpage](https://www.ctcms.nist.gov/fipy/INSTALLATION.html) has instructions on setting up a specific conda environment with important packages from conda-forge, and installing latest fipy through pip.

The visualization outputs are currently all over the place requiring 3 different packages - gifsicle, imagio, & moviepy. Future plans are to integrate all by only employing moviepy!






_P.S. It should likely work with python3 as well, though rigorous testing with other packages yet to be completed._
