# Jellyfin in Docker for CyberDeck Project


## Prerequisites
- Docker installed on your Raspberry Pi
- Docker Compose installed on your Raspberry Pi

## Files in This Repository
- docker-compose.yml
- README.md

## Instructions
### Step 1: Clone the Repository
Clone this repository to your Raspberry Pi:
```
git clone https://github.com/mikepaxton/ntp-server.git
cd ntp-server
```
### Step 2: Edit docker-compose.yml
Change user to the correct id number for admin
Change volumes to the location where you want to store these files:
/cache is for web files and such. /transcode is for video chunks created by ffmpeg to stream stuff.
- config - Keep in mind this config directory will grow in size as tv and movies are added.
- cache - Location where store temp transcode files.  
- video - Location of your tv and movie files.
- JELLYFIN_PublishedServerUrl= something like http://cyberworkstation.local

### Step 3: Run docker compose and verify container runs with no errors
`docker compose up`

### Step 3: If no errors, stop the container

`Ctrl + C`

## Additional Information
Currently, I've not been able to get the config directory to work on the external hard drive that videos on are.  I get a "SQLite Error 5 database locked" error.  I think it's a permissions issue but i've not solved it.
I'm running 

