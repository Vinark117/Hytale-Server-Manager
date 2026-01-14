# Hytale-Server-Manager
A linux shell script which when launched, automatically checks the latest server version, and updates the server files if there is a new version available. After verifying that the server files are up to date, the server will be launched.

# Setup
Create a folder for your servers. You can either place the program directly in the server folder and use relative folder paths (you just need to specify the folder name, not the full path), or create a separate folder for the manager and use full paths when launching servers.

The script uses the official hytale downloader to check for and download the latest server files. You can download it from the following link: https://downloader.hytale.com/hytale-downloader.zip

Once you have downloaded the file, extract it, and rename the linux program to `hytale-downloader` (no file extension). After you've renamed the file, move the downloader to the same folder where you've saved the `hytale-server-manager` script.

Run the hytale-downloader script once to authenticate yourself. Authentication is not possible when running the manager script, so you have to do it first. 

```sh
cd "pathToServerFolder"
./hytale-downloader -print-version

# follow steps to authenticate
```

# Usage

Once you've completed the setup, you can simply run the script with the following command in your terminal.

```sh
./hytale-server-manager "Server Folder Name" -rm
```

Arguments:
- `$1`: Server folder location, relative (if the manager is in the servers folder) or full path
- `$2`: You can type -rm if you don't wish to keep the server zip file after the update is complete, otherwise this argument can be skipped
