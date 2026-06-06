# Salatik static assets

Public static assets served over HTTPS for the [Salatik](https://github.com/highthem/Salatik) prayer-times app and Alexa skill.

## Structure

```
audio/
  adhan-fajr.mp3  # Fajr adhan
  adhan.mp3       # Regular adhan
```

## URLs

Files are served directly from GitHub's raw endpoint with valid HTTPS:

```
https://raw.githubusercontent.com/highthem/assets/main/audio/adhan-fajr.mp3
https://raw.githubusercontent.com/highthem/assets/main/audio/adhan.mp3
```

The Salatik Alexa skill can use this base URL:

```
ADHAN_AUDIO_BASE=https://raw.githubusercontent.com/highthem/assets/main/audio
```
