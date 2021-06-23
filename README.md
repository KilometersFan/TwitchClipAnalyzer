# Clip & Ship
## What is Clip & Ship?
The Clip & Ship is a standalone program designed to find and display significant moments of a livestream broadcast. 

The aim of Clip & Ship is to facilitate the common phrase "clip it and ship it". To do so, users can define categories of moments based on a broadcaster's Twitch, Better TTV, and FrankerFaceZ emotes (if available) and any other emote/word desired. 

For example, a user can define a "cool" category for the broadcaster supertf that includes suprPOG (twitch emote), LETSFUCKINGGOO (BTTV emote), PogU (FFZ emote), PogChamp, and cool (other emotes)

In addition to viewing and downloading all clipped moments of user-defined categories the program finds, users can also download specific time ranges of a vod or download the whole vod.

## Who benefits from Clip & Ship?
The intended users are content creators and video editors who want to streamline their workflow pipelines by quickly finding, viewing, and downloading specific types of clips within a broadcast. 

Additionally, there are some features for data scientists who may want to analyze the emotes used in broadcasts. However, everyone is welcomed to use Clip & Ship.

## Clip & Ship Features
### General Features
- Search for and select channels you want to analyze.
- Create custom categories based on a channel's Twitch emotes, Better TTV emotes, FrankerFaceZ emotes, and other emotes.
- If a channel's videos have been processed, the TCA can provide emote recommendations for new or existing categories.
- Find the latest VODs for a channel to process. 
- Process a broadcaster's VOD and get a list of clips for each category you created for that channel.
- Process multiple VODs from several channels simultaneously.
- Watch all the clips analyzed from a VOD with a builtin clip results viewer to determine which timestamps you want to use for your video(s).
- Download the clips generated by the program, download a specific time range of the VOD, or download the whole VOD.
- Filter results by category and view the similarity between the emotes used in the clip, and the category label(s) assigned to the clip.
- View the emote usage by category per clip with detailed graphs.
### Advanced Features
- Export emote data to a csv file for every processed VOD
- Export all the emote groups found for every channel.
- Upsample the data to even out category weights if imbalance occurs with the data_exporter.py file.

## Requirements

- Modern browser. This app creates a new window in Google Chrome or your default browser (if Chrome isn't installed). 
- If running locally you need Python3, [eel](https://github.com/ChrisKnott/Eel), [plotly](https://plotly.com/), [pandas](https://pandas.pydata.org/), [numpy](https://numpy.org/), [configparser](https://docs.python.org/3/library/configparser.html), and [twitch-python](https://github.com/PetterKraabol/Twitch-Python), among other things. See the ```requirements.txt```

## Local Development
Install the required libraries. To run the main program change directory to ```src``` and run ```python3 clipnship.py```. To run the data_exporter program, run ```python3 data_exporter.py``` in the same directory. The upsampler will only work if the you processed at least one video for the specified channel.

## Example
### Adding a Channel
<img width="1278" alt="Screen Shot 2021-06-11 at 1 17 02 PM" src="https://user-images.githubusercontent.com/35278719/121744151-517e7500-cab7-11eb-8246-0bab0c54d0f0.png">

### Viewing the Channel Settings
<img width="1258" alt="Screen Shot 2021-06-11 at 1 17 32 PM" src="https://user-images.githubusercontent.com/35278719/121744182-622eeb00-cab7-11eb-83b1-3a622da7f713.png">

### Adding a Category
<img width="1257" alt="Screen Shot 2021-06-11 at 1 18 21 PM" src="https://user-images.githubusercontent.com/35278719/121744267-7f63b980-cab7-11eb-8cbc-f4c08b6de3e7.png">

### Viewing a Channel's VODs
<img width="1262" alt="Screen Shot 2021-06-11 at 1 18 41 PM" src="https://user-images.githubusercontent.com/35278719/121744305-8b4f7b80-cab7-11eb-88ab-e38a9fd5f932.png">

### Processing a VOD
<img width="1279" alt="Screen Shot 2021-06-11 at 1 18 56 PM" src="https://user-images.githubusercontent.com/35278719/121744331-94404d00-cab7-11eb-9e8e-0a13f94b75f7.png">

### Finishing VOD Processing
<img width="1278" alt="Screen Shot 2021-06-11 at 1 23 13 PM" src="https://user-images.githubusercontent.com/35278719/121744735-2d6f6380-cab8-11eb-8ba9-2904290ecaa0.png">

### Viewing VOD Results
<img width="1259" alt="Screen Shot 2021-06-11 at 1 23 25 PM" src="https://user-images.githubusercontent.com/35278719/121744759-34967180-cab8-11eb-9842-0dcc5c5ad3b4.png">

### Inspecting a Clip
<img width="1262" alt="Screen Shot 2021-06-11 at 1 24 02 PM" src="https://user-images.githubusercontent.com/35278719/121744797-4aa43200-cab8-11eb-88de-5e2a4d9ecf2b.png">

## Limitations
- The executable takes a while to start up, so please be patient when opening it (this is an issue with PyInstaller).
- Everything is stored locally. All analysis, channel categories, and channel info is on your machine, not on the cloud. Make sure you have plenty of storage.
- Similarly, analysis performance is based on your machine. A computer with more cores, and a fast processor will run analysis faster than a worse machine.
- Reliance on third party technologies. This app uses BTTV, FrankerFaceZ, and Twitch APIs. If any of these companies change something to their API, the app may not work correctly. In that case, please report problems on the issues page.
- The Clip & Ship works well with channels that have emote-heavy chats but performs poorly if the chat doesn't frequently use emotes.

Feel free to ask questions or report bugs on the issues page.
