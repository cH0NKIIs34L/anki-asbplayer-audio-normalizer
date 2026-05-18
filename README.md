# Anki asbplayer Audio Normalizer

A highly configurable PowerShell script utilizing FFmpeg to batch-normalize the volume of audio files clipped via **asbplayer** for Japanese language mining notes.

## Setup

1. Make sure you have [FFmpeg](https://ffmpeg.org/) installed and added to your system's PATH.
2. Open `config.json` and adjust the `"MediaDirectory"` string to match your local Anki user profile path.

## Usage

Open PowerShell inside this directory and run one of the following commands:

### Run on all historical files:

```powershell
.\Normalize-AsbPlayerAudio.ps1
```

### Run only on audio clipped today:

```powershell
.\Normalize-AsbPlayerAudio.ps1 -TodayOnly
```
