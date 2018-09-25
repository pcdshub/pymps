# PYMPS
Python Interface for L2S-I Photon MPS system

The `calculation_template.ipynb` is a Jupyter Notebook intended to demonstrate
how properties of a component's material are converted into concrete
requirements for both photon attenuation and pulse rate.

## Usage
The calculation assumes you have a pre-assembled table of component
requirements. There are a few instances of these tables contained inside the
`examples` directory for reference. If you wish to read through the
calculations interactively simply open the notebook and step through it as
directed. You will however have to point the `req_file` variable to point to
your requirements table.

```bash
$ jupyter-notebook calculation_template.ipynb
```

The other option is to use `papermill` to execute the notebook as a script. In
this case, the entire notebook is run and a copy of the completed version is
saved for record. In this case you can pass in the path to the requirements
file via the command line.
```bash
$ papermill calculation_template.ipynb yag.ipynb -p req_file examples/yag.csv 
```
## Installation
The `requirements.txt` file contains all the necessary Python packages for
using the Jupyter Notebook. Either:

```bash
$ pip install -r requirements.txt
```
or
```bash
$ conda install --file requirements.txt -c conda-forge
```
