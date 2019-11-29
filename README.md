# food-recognition network

## get started

- Setup a virtual environment and install packages.
 
- Download the data either directly from the site or use the Kaggle API.

- run data formatting script to create a structured training set directory with unique label named subdirectories containing examples of that class.

```
# make virtual environment
python3 -m venv env

# activate environment
source env/bin/activate

# download packages
pip install -r requirements.txt

# create API key on your kaggle account

# move API key to correct directory
mv kaggle.json home/<your username>/.kaggle

# make /data folder, download data from kaggle and unzip it
mkdir data; kaggle competitions download -c food-recognition-challenge; unzip food-recognition-challenge.zip;

# run the data formatting script
python data_formatter.py

```

## best practice

- run smaller models locally on your CPU or GoogleCollab to test performance of your model.
- once models have been developed and work, commit your model to `/models` folder and it can be run on full dataset using `V100` GPU on Google Compute Engine.

## development environment

- you can run a jupyter-notebook inside your virtual environment as specified by this [guide](https://anbasile.github.io/programming/2017/06/25/jupyter-venv/)
- download data and run it inside a kaggle kernel and make use of their free GPU resources (requires phone verification).
