# YouTube Video Uploader

This Python script allows you to upload videos to YouTube using the YouTube Data API.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/bishal-dahal/Python-Youtube-Uploader/blob/main/Uploader.ipynb)

## Requirements

This script requires the following Python packages:

- httplib2
- google-api-python-client
- google-auth
- google-auth-httplib2
- google-auth-oauthlib

You can install these packages using pip:

```bash
pip install -r requirements.txt
```

## How it works

The script uses the Google API client library to interact with the YouTube Data API. It authenticates with Google's OAuth 2.0 service using a `client_secrets.json` file, which contains the client ID and client secret for your application.

The script first checks if a token file (`token.pickle`) exists. If it does, it loads the credentials from it. If the token file does not exist or the credentials are invalid, it prompts the user to log in and then saves the credentials for the next run.

The script uses these credentials to build a service object for the YouTube Data API. It then initializes the upload process for each video file in the `videos` directory. The title, description, category, keywords, and privacy status of the videos can be specified with command line arguments.

The script uses a resumable upload process, which allows it to resume the upload if it is interrupted. It implements an exponential backoff strategy to handle HTTP errors and other exceptions that can be retried.


# Usage
To use this script, you need to provide it with a `client_secrets.json` file from the Google API Console. This file should contain the OAuth 2.0 information for your application, including its client_id and client_secret.

Once you have your client_secrets.json file, you can run the script with the following command:
```bash
python upload.py
```


By default, the script will upload all video files in the `videos` directory. You can specify the title, description, category, keywords, and privacy status of the videos with command line arguments. For more information on these arguments, run:
```bash
python upload.py --help
```


# License
This project is licensed under the terms of the MIT license.
