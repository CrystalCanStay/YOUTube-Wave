# YOUTube-Wave

# Overview
YOUtube Wave is a dedicated locally run youtube to .wav converter for linux. Its currently built off of selenium to get link metadata, mpv for for playing videos, and pipewire for recording. To use, install the requirements, fill the links.txt file with youtube links, run main, and wait till it finishes! This program works by playing music and then recording your soundcard to get a final .wav file. Quality is not 1-1, nor is it perfect as an original file straight out of a DAW due to youtube compression, and re-encoding.
# Setup
For ubuntu based distros (since mpv/yt-dlp is not updated properly on this platform), run:
```
sudo apt update
sudo apt install google-chrome-stable
sudo apt install mpv

# cd into this directory
sudo mv -i requirements/yt-dlp /usr/bin
# Select yes if it asks to replace
```

For arch or fedora or Nix:
Install google-chrome. Install mpv, make sure it is on a recent version with a recent version of yt-dlp installed on it (usually located in /usr/bin). You are welcome to move the included yt-dlp file into the right place yourself. Just follow the ubuntu/debian based instructions but use nix or pacman or yay or whatever package manager gets you mpv added to your system.

Note:
If you wan to be extra cautious and are worried about youtube IP banning you, use a vpn to bypass it. This will probably not happen, but if you're worried, feel free to.

# Running
Go to the directory where this program is located, open the links.txt file, and fill it with youtube links. Note, only use valid youtube links (youtube.com or youtu.be), leave one new empty line after the final link, and remove all non-imporant url modifiers to the youtube link. For example: https://youtu.be/oYlcUbLAFmw?si=obHY3ZVOKzxhKCCG should be reduced to https://youtu.be/oYlcUbLAFmw. Notably as well, videos inside playlists are untested. After this, run the main program, choose what you would like (option 1 uses the links.txt, option 2 lets you input a link), and wait for it to finish. Output files are put into a generated "Output" folder in this same directory.

# Notice
I am not legally responsible for how this tool is used, furthermore this tool should only be on videos that the creator and all parties inbetween have consented to being downloaded into a .wav file. Abide by local regulations during use.
