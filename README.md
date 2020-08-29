# How to restream an MP3 stream to your own IceCast MP3 stream
- sudo apt-get install libasound2 libasound2-plugins alsa-utils alsa-oss
- sudo apt-get install pulseaudio pulseaudio-utils
- sudo usermod -aG pulse,pulse-access <username>
- pulseaudio -D
- sudo reboot
- cvlc -vvv --color http://open.live.bbc.co.uk/mediaselector/5/select/version/2.0/mediaset/http-icy-mp3-a/vpid/bbc_radio_two/format/pls.pls --sout '#standard{access=shout{mp3},mux=raw,dst=your_icecast_username:your_icecast_password@radio.example.com:8005/}'
