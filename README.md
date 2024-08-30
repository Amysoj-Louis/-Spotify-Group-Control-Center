# Spotify-MultiJam

**NOTE:** ⚠️ *This script does not align with Spotify's usage terms. Use at your own risk.*

## Overview

**Spotify-MultiJam** is an unofficial Python script that allows you to remotely control multiple Spotify accounts concurrently. With this tool, you can manage playback (play, pause, resume) and search for tracks across all your Spotify devices simultaneously.

## Features

- **Multi-Account Control**: Control playback on multiple Spotify accounts at the same time.
- **Concurrent Execution**: Commands are executed concurrently across all accounts, ensuring synchronized playback.
- **Search and Play**: Search for tracks and play them on selected devices.
- **Fuzzy Command Matching**: Handles typos and variations in command inputs.

## Prerequisites

Before using the script in python, ensure the following:
- Install the required Python packages:
  ```
  pip install requests beautifulsoup4 python-Levenshtein
  ```

## How to Use

### Step 1: Retrieve Your `sp_dc` Tokens

1. Open your web browser and go to [Spotify's Web Player](https://open.spotify.com).
2. Log in to your Spotify account.
3. Open Developer Tools in your browser:
   - For **Google Chrome** / **Mozilla Firefox**: Press `Ctrl + Shift + I` (Windows/Linux) or `Cmd + Option + I` (Mac).
   - For **Microsoft Edge**: Press `F12`.
4. Navigate to the **Application** tab (in Chrome/Edge) or **Storage** tab (in Firefox).
   - In the left sidebar, look for **Cookies** under the **Storage** section.
   - Click on `https://open.spotify.com` to view the list of cookies.
5. Locate the cookie named `sp_dc`.
   - The value of the `sp_dc` cookie is your token.
6. Copy the value of the `sp_dc` token and paste it into the `tokens` list in the script.

### Step 2: Add Your Tokens

- Open the script and locate the `tokens` list.
- Add your `sp_dc` tokens as string values in the list:
  ```python
  tokens = [
      "your_first_token_here",
      "your_second_token_here"
  ]
  ```

### Step 3: Run the Script (If you are using python)

- Run the script in your Python environment:
  ```
  python main.py
  ```

- Follow the on-screen instructions to control your Spotify devices.

## Commands

You can enter the following commands:

- **play**: Play a track on all devices. You will need to provide a Spotify track URI.
- **pause**: Pause playback on all devices.
- **resume**: Resume playback on all devices.
- **search**: Search for a track across all connected Spotify accounts. You can select a track to play by its number.
- **exit**: Exit the script.

## Disclaimer

This script is unofficial and for educational purposes only. It is not endorsed by Spotify, and using it may violate Spotify's terms of service. Use at your own risk.
