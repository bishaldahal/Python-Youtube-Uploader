# YouTube Video Uploader

This Python script allows you to upload videos to YouTube using the YouTube Data API.

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

# Usage
To use this script, you need to provide it with a client_secrets.json file from the Google API Console. This file should contain the OAuth 2.0 information for your application, including its client_id and client_secret.

Once you have your client_secrets.json file, you can run the script with the following command:
```bash
python upload.py
```


By default, the script will upload all video files in the videos directory. You can specify the title, description, category, keywords, and privacy status of the videos with command line arguments. For more information on these arguments, run:
```bash
python upload.py --help
```


# License
This project is licensed under the terms of the MIT license.
