This folder captures the attempts to create a starter template for Martin Vector Tile Server + MapLibre.


How to start?
1) Follow the quickstart for Linux at the following link. This will start a Martin Tile Server. Refer: https://maplibre.org/martin/quick-start-linux.html. These steps were carried on a Windows 10 machine in the WSL environment.
2) The file used for starting the fileserver was in local storage E.g."india-latest.pmtiles , asia.pmtiles, bhutan.pmtiles etc. Create these files using methods noted in the slide deck (power point presentation) at following link: https://github.com/maplibre/workshop
3) Use the proposed startercode(s) index.html in this github repository and open the folder where index.html resides using VSCode Insiders.
4) Use the Live Server extension in VSCode Insiders to open the index.html file and view the output map at the Live Server localhost:port.(This port can be configured in settings for Live Server).


Log
- Can see some water bodies and landuse probably figures in there. Definetely need a style.json file.
- Can see names, but it still does not look  like a map. Baseline startercode 2
- Startercode4 refers to bhutan9.pmtiles map generated using Tilemaker using openmaptiles configuration specified at the following links: https://github.com/systemed/tilemaker/tree/master/resources
- Startercode5 updated with the correct URL so that the fonts seem to have been picked.
- Following command issued in martin server folder to kickoff martin with fonts. 
- martin$ ./martin --font ./MartinStarter/fonts/open-sans/OpenSans-Regular.ttf  /mnt/c/data/asia.pmtiles
- note that the font path is now relative to where the martin binary is invoked from whilst the pmtiles path is a full path from /mnt in WSL.
- Startercode 6 will be further investigated for future work noted below. 


Issues observed/ Future Work
- Note: Martin tileserver vs tileserver-GL is a good comparison because quite a lot of critical aspects of the pmtiles file are being highlighted.
- Issue noted with zoom level: Martin for asia.pmtiles with Startercode5 is not giving good zoom in after 14. Whilst this is not an issue with tileserver-GL. Why? Perhaps need to check Log from Wireshark and understand if tileserver-GL's better performance is based on data retrieval from external sources.
