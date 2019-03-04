## Create a new environment
conda create -n [Env Name]

## Create a new kernel for jupyter notebook (Perform this from your activated environment)
python -m ipykernel install --user --name pandas_cub --display-name "Python [EnterVersion] ([Enter Env Name])"

## Move to environment folder and create activate/deactivate scripts. 
cd %CONDA_PREFIX%<BR>
mkdir .\etc\conda\activate.d<BR>
mkdir .\etc\conda\deactivate.d<BR>
type NUL > .\etc\conda\activate.d\env_vars.bat<BR>
type NUL > .\etc\conda\deactivate.d\env_vars.bat<BR>

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
