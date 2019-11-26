# food-recognition network

## get started

- Setup a virtual environment and install packages.
 
- Download the data either directly from the site or use the Kaggle API.

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

```

## best practice

- run smaller models locally on your CPU or GoogleCollab to test performance of your model.
- once models have been developed and work, commit your model to `/models` folder and it can be run on full dataset using `V100` GPU on Google Compute Engine.
