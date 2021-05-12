# Converting video files to MP4

This simple script uploads a video file and converts it with **ffmpeg** to **mp4** format.

Cheers!

## Automatic installation

You can follow this automatic script (make sure you are in the root directory of the website).
```bash
sudo chmod 750 ./install.sh && sudo ./install.sh
```

Or you can do it all manually using the rest of this readme below.

WARNING: If you already did the automatic installation from above you don't need to follow the next steps! You are already ready to go :)


## Requirements


You need **ffmpeg** to be able to convert.

On Mac OS with Homebrew:

```bash
brew install ffmpeg
```

On Ubuntu:

```bash
sudo apt install ffmpeg
```


## Installation

No installation besides the above needed. Just make sure you have the right file permissions.

```bash
sudo chmod -R 775 ./original ./converted && sudo chmod 770 ./cleanup.php && sudo chmod 750 ./install.sh && sudo chmod 750 ./log.txt
```

## Automatic cleanup

You can also make a cronjob to automatically delete uploaded and converted videos older than 1 day if you want.
```bash
sudo crontab -e
```

Paste the following at the end of the file (just make sure the path is where your app is located):
```bash
0 * * * * /var/www/html/cleanup.php
```
