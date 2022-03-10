# Google Cloud Functions
## New Functions Project

To start a project go to [Firebase Console](https://console.firebase.google.com/) or create it from [Google Cloud Platform Console](https://console.cloud.google.com/)


# Creating a virtual environment
Install `python3-venv` using:
```
sudo apt install python3-venv
```
Then execute this command to create a folder called venv

```
python3 -m venv venv
```

Finally, to activate this virtual environment run:

```
source venv/bin/activate
```

To add new packages to the virtual environments, you have to create a file called `requirements.txt` and to install those packages, run this command:
```
pip install -r requirements.txt
```

To test code in local, just run:
```
functions-framework --target hello_world --debug --port 8000
```

## Deploying GCP Functions
To deploy into GCP, you have to :

Get your project ID by running this command:
```
gcloud projects list
```

Set your project ID:

```
gcloud config set project <PROJECT_ID>
```

Enable Cloud Build API by visiting -> [Cloud Build API](https://console.developers.google.com/apis/api/cloudbuild.googleapis.com/overview?project=272914054599)


And finally, deploy your functions, by running:
```
gcloud functions deploy hello_world --runtime python38 --trigger-http
```