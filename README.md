# VALORANT RPC
![Static Badge](https://img.shields.io/badge/Build-2.0-green)
![Static Badge](https://img.shields.io/badge/Development-2.0-red)

Show your current VALORANT competitive rank via Discord Rich Presence.

The app displays your rank, RR, and rank icon in Discord while keeping the setup simple:

```text
Rank: Diamond 2
RR: 74 / 100
```

## Download

1. Open this GitHub page's **Releases** section.
2. Download `ValorantRPC.exe` from the latest release.
3. Put `ValorantRPC.exe` in its own folder, for example:

```text
C:\Users\YourName\Apps\ValorantRPC
```

Windows SmartScreen may warn you because this is an unsigned community executable. Choose **More info** and **Run anyway** only if you trust the download source.

## Requirements

- Windows
- Discord desktop app installed and running
- A HenrikDev API key
- A Riot ID, for example `Player#EUW`

## Get A HenrikDev API Key

Create or copy your HenrikDev API key from [HenrikDev](https://api.henrikdev.xyz/dashboard/), then configure it using one of the options below.

The API key is only used locally by the app. It is not stored in `config.json`.

## Option 1: Use A `.env` File

In the same folder as `ValorantRPC.exe`, create a file named:

```text
.env
```

Put this inside:

```text
HENRIKDEV_API_KEY=YOUR_API_KEY_HERE
```

Then start `ValorantRPC.exe`.

## Option 2: Use A Windows Environment Variable

Open Command Prompt and run:

```bat
setx HENRIKDEV_API_KEY "YOUR_API_KEY_HERE"
```

After running `setx`, fully close and reopen `ValorantRPC.exe`.

## How To Use

1. Open Discord.
2. Open `ValorantRPC.exe`.
3. Enter your Riot name.
4. Enter your Riot tag without `#`.
5. Choose `PC` or `Console`.
6. Choose whether to show your Riot ID using the **Show Name** switch.
7. Choose whether to show leaderboard position using the **Leaderboard Pos** switch.
8. Click **Start RPC**.

Example:

```text
Riot Name: Player
Riot Tag: EUW
```

If **Show Name** is enabled, Discord's large image tooltip shows:

```text
Player#EUW
```

If **Show Name** is disabled, it shows:

```text
VALORANT
```

If **Leaderboard Pos** is enabled and your account is on the leaderboard, the rank icon tooltip shows:

```text
#123
```

If your account is not on the leaderboard, the rank icon tooltip stays as your rank.

## Saved Settings

The app creates `config.json` in:

```text
%APPDATA%\empty.src\ValorantRPC\config.json
```

It stores:

- Riot name
- Riot tag
- Platform
- Show Name preference
- Leaderboard Pos preference

It does not store your HenrikDev API key.

## Updating

1. Close `ValorantRPC.exe`.
2. Download the newest `ValorantRPC.exe` from Releases.
3. Replace your old `ValorantRPC.exe` with the new one.
4. Open the app again.

Your saved settings stay in `%APPDATA%\empty.src\ValorantRPC\config.json`.

## Screenshots

![App Screenshot](https://i.gyazo.com/55e473dececdd476132d2e17dd803ba9.png)

![App Screenshot](https://i.gyazo.com/13415b4aab34384e4c7018e6afc8298e.png)

## Troubleshooting

**Discord was not detected**  
Open the Discord desktop app, wait a few seconds, then click **Start RPC** again.

**HENRIKDEV_API_KEY is not set**  
Create a `.env` file next to `ValorantRPC.exe` or set the Windows environment variable.

**Player not found**  
Check the Riot name and tag. Do not include `#` in the tag field.

**API rate limited**  
Wait a few minutes and try again.

**Windows will not let you replace the EXE**  
Close every running `ValorantRPC.exe` window before replacing the file.
