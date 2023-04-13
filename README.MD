# This script help to synchronise a local folder with you Google Drive folder

The original repositores are :
* [pedronogs : auto-sync-drive](https://github.com/pedronogs/auto-sync-drive)
* [HowStrange : sync-googledrive](https://github.com/HowStrange/sync-googledrive)

I just add some modification and adapt it for Linux, my next task is to build graphical interface with Tkinter or make a web-app with using Flask.
For Windows user you can see those above link and adapt it.

**Note :** I am note responsible for any loss of your data, use it at your own risk


How to use it :
It is better to create virtual environment if possible :
You can use the following command (In your console) and inside the folder containing this script.

**Before to start you should activate you google API:**
This is the step :
1. Go to https://console.developers.google.com/ and log in with the Google account connected to the Google Drive you want to access.
2. Click on “Credentials” in the left-hand menu.
3. Click on “Create credentials” and select “OAuth client ID.”
4. Choose application type : Desktop app
5. Put a name for example: Sync_GoogleDrive_and_Local.
6. Click on Create.
7. On the pop-up click Download json
8. Locale a file starting by "client_secret_......" in your download folder.
9. Rename it to "credentials.json" and put it in the same folder as the python script


**Setting the apps**
1. Create the virtual environment
```
python -m venv venv
```
2. Activate the virtual environment
```
source venv/bin/activate
``` 

**Then the following command will be the same for all (with or without virtual environment)**

3. Install required python packages
```
pip install -r requirement.txt
```

4. Setting 
    * Open your Google Drive folder, the one where you want to synchronise : and copy the last parameter on the link like this:
    ![](assets/drive_id.png)
    * Open the config.json, you will see this :

    ```{json}
    {
    "drive_folder_id": "ID_OF_YOUR_GOOGLE_DRIVE_FOLDER",
    "local_folder_path": "~/PATH/TO/YOUR/LOCAL/FOLDER",
    "log_file_path": false
    }```
Fill the required information, and save it.


5. Run 'gSync.py'
```
python up_down_GDrive.py
```

On the first time it will open your web browser to ask for the authorization to have the access on your Google Drive through your gmail account. And if everything is okay, The synchronisation will start.


And every time you want to synchronise your folder, just do the step 5.



