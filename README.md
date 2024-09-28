# Gemini-Flipper

Currently in development stage, here I'm going to upload the .js code that I currently use so that anyone who wants to join and help improve it can make their PRs and also for those C developers who want to help create the native Flipper app and be accessible by everyone from https://lab.flipper.net/apps

# How it is work

Currently the code takes the api key in plain text stored in:

"/ext/apps_data/gemini_ia/key.txt"

it reads the .txt file and sends it via serial command to the esp32 as soon as the app is initialized (it would be nice to implement some kind of encryption to the api key but it is important that it is sent in plain text and unencrypted to the esp32 because this is how the firmware can read and implement it)

About saved APs: when the user connects to a new AP the information needed to connect again is stored in "/ext/apps_data/gemini_ia/SavedAPs.txt" I need to improve the way it saves the information because it overwrites the other AP you have saved

# TO DO

--> improve the handling of how the APs are saved, currently it saves them but rewrites the previous one

--> improve the handling of how the saved APs are sent to the esp32 to avoid re-entering the SSID and password (Improving the previous point this should solve itself)

--> load the firmware binary for the esp32 (nothing to do here just load the binary)

# Screenshots

![image](https://github.com/user-attachments/assets/3878b4a2-223d-4d23-b395-2d25cf710fed)

![image](https://github.com/user-attachments/assets/777e2d55-f9fd-4c63-bb47-450b020b80e0)
