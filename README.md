# Salatik static assets

Public static assets served over HTTPS for the [Salatik](https://github.com/highthem/Salatik) prayer-times app and Alexa skill.

## Structure

```
audio/
  adhan_<prayer>_<voice>.mp3        # 128 kbps stereo, full recitation (~3-5 MB)
  adhan_<prayer>_<voice>_short.mp3  # 48 kbps mono, ≤240s (for Alexa SSML <audio>)
```

Where:
- `<prayer>` ∈ `fajr`, `regular`
- `<voice>` ∈ `madinah`, `mecca`, `alaqsa`

## URLs

Files are served directly from GitHub's raw endpoint with valid HTTPS:

```
https://raw.githubusercontent.com/highthem/assets/main/audio/adhan_fajr_madinah.mp3
```

The Salatik Alexa skill builds these URLs at runtime using the env var:

```
ADHAN_AUDIO_BASE=https://raw.githubusercontent.com/highthem/assets/main/audio
```

## Sources & licenses

- **Madinah Fajr** — Sheikh Faisal Numan, **CC0 1.0 Universal** ([Internet Archive](https://archive.org/details/MadinahFajrAzan))
- **Mecca / Al-Aqsa / regular Madinah** — recordings from the [Internet Archive "TataCaraAdzan" community collection](https://archive.org/details/TataCaraAdzan); commonly redistributed broadcasts of state-run mosque feeds. Verify per-recording rights before commercial redistribution.

See `Salatik/assets/audio/SOURCES.md` in the main app repo for the full attribution table.
