# karaokio
Make Karaoke video from Youtube video.
Separate source audio into vocals, bass, drums and other instruments.

- Download mp4 video from YouTube
- crop video clip
- Extract mp3 audio out of the video
- convert the mp3 to .wav --> numpy array
- run source-separation
- write the multiple tracks to multiple mp3's
- remix the audio
- combine the remixed audio with the video


Work log:

## 2023-03-12
- Use open-unmix to perform source sepation, which supports vocals, drums, bass and group the remaining as "others"
- I found that [https://vocalremover.org/](https://vocalremover.org/splitter-ai) provides better quality than this off-the-shelf open-unmix.
- Another similar app https://vocali.se/en provides only karaoke (vocal + others), which is quite limited.

## TODO:
- Try more source separation packages from this [list on demucs 4.0.0](https://pypi.org/project/demucs/).
- spleeter seems to be among the top, so need to get it to work.
    - I found it's very hard to install
- Checkout which packages they use for:
    - [splitter.ai](https://splitter.ai/) provides piano extractor
    - [https://vocalremover.org/](https://vocalremover.org/splitter-ai) provides guitar extractor


