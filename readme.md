[Activate/Deactivate Environment Variables](#envvars)
# Environment Creation

## Create a new environment
##### Start A New Env
conda create -n [Env Name] [Packages to install, IE python=3.7 numpy pandas or none for full anaconda install]<br>

##### From Env.yml file
conda env create -n conda-env -f [/path/to/environment.yml] 

## Add packages to and environment from an env.yml file
conda env update -n conda-env -f /path/to/environment.yml

## Create a new kernel for jupyter notebook (Perform this from your activated environment)
python -m ipykernel install --user --name pandas_cub --display-name "Python [EnterVersion] ([Enter Env Name])"

## Move to environment folder and create activate/deactivate scripts. 
cd %CONDA_PREFIX%<BR>
mkdir .\etc\conda\activate.d<BR>
mkdir .\etc\conda\deactivate.d<BR>
type NUL > .\etc\conda\activate.d\env_vars.bat<BR>
type NUL > .\etc\conda\deactivate.d\env_vars.bat<BR>

# Environment Variables On Activate And Deactivate
<div id='envvars'/>
## env_vars.bat for actvation
@echo off<BR>
set DRIVE=[enter code drive here]<br>
%DRIVE%<BR>
set BASE_DIR=[Add project code dir here]<BR>
CD %BASE_DIR%<BR>

## env_vars.bat for deactvation
@echo off<BR>
set DRIVE=<BR>
set BASE_DIR=<BR>

## Export Environment to environment.yml file
conda env export > environment.yml

## Create environment from environment.yml file
-----------------------------------------------
conda env create -f environment.yml
