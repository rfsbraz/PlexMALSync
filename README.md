# Plex to MyAnimeList Sync

If you manage your Anime with Plex this will allow you to sync your libraries to MyAnimeList.net, recommend using Plex with the [HAMA agent](https://github.com/ZeroQI/Hama.bundle) for best Anime name matches.

Unwatched Anime in Plex will not be synced so only those that have at least one watched episode, updates to MAL are only send with changes so need to worry about messing up watch history.

Currently planned for future releases:

- Error handling
- CLI improvements (colors / status / user input etc..)
- Improve matching by using more MAL info, year comparision is an option but was hit and miss during testing before
- Multiple season support, right now sync is limited to season 1 and not sure if feasible with the way MAL lists them 

Previous version was written in C# (.NET) but due to library issues switched to Python where there are some great ones to work with, this is the first version and rough around the edges so bugs may occur.

## Installation

### Step 1 - Configuration

Open PlexMALSync.py with your favorite editor and change the configuration section at the top (authentication / section), for Plex you need to select one authentication method (MyPlex OR Direct IP)

### Step 2 - Install requirements

Install  requirements from requirements.txt using this python command in the project folder:

- pip install -r requirements.txt

### Step 3 - Start syncing

Now that configuration is finished and requirements have been installed we can finally start the sync script:

- Python PlexMALSync.py

Depending on library size and server can take a few minutes to full sync, logging is verbose at the moment but will show the progress per show and when finished.

## Requirements

[Python 3 (tested with 3.6.4)](https://www.python.org/)

## Support

Support thread is located on Plex Forums:

https://forums.plex.tv/discussion/305261/plexmalsync-sync-your-plex-library-to-myanimelist

## Credits

[Python-PlexAPI](https://github.com/pkkid/python-plexapi)

[Spice](https://github.com/Utagai/spice)
