# Anki asbplayer Audio Normalizer

A highly configurable PowerShell script utilizing FFmpeg to batch-normalize the volume of audio files clipped via **asbplayer** for Japanese language mining notes.

## Setup

1. Make sure you have [FFmpeg](https://ffmpeg.org/) installed and added to your system's PATH.
2. Open `config.json` and adjust the `"MediaDirectory"` string to match your local Anki user profile path.
3. If PowerShell blocks the script with an `UnauthorizedAccess` or `PSSecurityException` error, run this once:

```powershell
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
```

To check whether PowerShell can find FFmpeg, run:

```powershell
ffmpeg -version
```

If that command is not recognized, install FFmpeg or add the folder containing `ffmpeg.exe` to your Windows PATH, then open a new PowerShell window.

## Usage

Open PowerShell inside this directory and run one of the following commands:

### Run on all asbplayer files:

```powershell
.\Normalize-AsbPlayerAudio.ps1 -All
```

### Run only on audio clipped today:

```powershell
.\Normalize-AsbPlayerAudio.ps1 -TodayOnly
```

### Preview matching files without changing them:

```powershell
.\Normalize-AsbPlayerAudio.ps1 -All -Preview
```

### Run from File Explorer:

Right-click `Normalize-AsbPlayerAudio.ps1`, select **Run with PowerShell**, then choose whether to process all asbplayer audio files or only today's asbplayer audio files when prompted.
