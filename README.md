# Studying Heart Rate Zones with Fitbit Data

This repository is a collection of Jupyter notebooks to compute my heart rate zones using Fitbit tracking data. 

## Installation

### Setting Up the Environment

The first thing you will need to do is install Jupyter with a Python3 kernel. 
The Python kernel should have access to the libraries listed in `requirements.txt` and [python-fitbit](https://github.com/orcasgit/python-fitbit). 

### Getting the Required Keys

You will also need to set up a Fitbit web app in order to access your data via the Web API. 
First, go to [dev.fitbit.com](https://dev.fitbit.com/apps/new) and create a new Web App. 
Your web app must be a 'Personal' type, and the callback should be `http://127.0.0.1:8080/`. 
I also chose 'Read Only' access, as I did not want to give myself the power to mess up my Fitbit data.

Once complete, copy the Client ID and secret into their places in the `client-data.json` file.
Next, use the `gather_keys_oauth2.py` utility from [python-fitbit](https://github.com/orcasgit/python-fitbit/blob/master/gather_keys_oauth2.py) to get the Access and Refresh keys for your app.
Copy the keys into `client-data.json`.

## Running

Run the notebooks in the following order:
- `get-activities.ipynb` to get a list of active days.
- `get-fthr.ipynb` to determine my FTHR and heart-rate zones