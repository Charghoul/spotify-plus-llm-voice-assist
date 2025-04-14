# Spotify Plus LLM Voice Script Blueprint


A Home Assistant blueprint that enables natural language voice control for the Spotify Plus integration using Home Assistant's voice assistant with LLM capabilities.

## Overview

This blueprint creates a script that allows you to control your Spotify Plus integration through natural language voice commands processed by Home Assistant's LLM-powered voice assistant. It improves upon the traditional intents-based approach by leveraging the LLM's ability to understand context and extract relevant information from your voice requests.

### Features

- Play music by artist, album, track, or playlist
- Control playback (shuffle, volume, etc.)
- Play podcasts and artist radio stations
- Specify which player or area to play on
- Supports direct Spotify URIs and search terms

## Prerequisites

- Home Assistant (2024.6.0 or newer)
- [Spotify Plus integration](https://github.com/thlucas1/homeassistantcomponent_spotifyplus) installed and configured
- A Home Assistant voice assistant with LLM capabilities (e.g., Assist with OpenAI, LocalAI, etc.)
- A Premium Spotify subscription

## Installation


1. Go to **Settings** > **Automations & Scenes** > **Blueprints**.
2. Click the **Import Blueprint** button.
3. Paste this URL `https://github.com/Charghoul/spotify-plus-llm-voice-assist/blob/main/spotify-plus-llm-voice-script.yaml`
4. Click **Import Blueprint**.

## Setup

1. Go to **Settings** > **Automations & Scenes** > **Scripts**.
2. Click the **Create Script** button.
3. Choose the **LLM Script for Spotify Plus voice requests** blueprint.
4. Configure the settings:
   - Select your default SpotifyPlus player.
   - Adjust the search limit if needed.
   - Review the prompt settings for LLM (usually the defaults work well).
5. Click **Save**.
6. Make the script available to your voice assistant:
   - Go to **Settings** > **Voice Assistants**.
   - Select your assistant.
   - Under **Exposed Entities**, make sure your new script is exposed.

## Usage

After setup, you can use your voice assistant to control Spotify Plus with natural language commands like:

- "Play music by Queen"
- "Play the song Bohemian Rhapsody"
- "Play the playlist Workout Mix"
- "Shuffle songs by The Beatles"
- "Play the podcast Serial"
- "Play Queen Radio"
- "Play some jazz music in the living room"

The script will:
1. Process your request using the LLM
2. Identify what type of media you want to play (track, artist, album, etc.)
3. Search Spotify if needed
4. Set shuffle mode appropriately
5. Play the requested content on your chosen player or area

## Customization

You can customize how the LLM interprets your requests by editing the prompt settings in the blueprint configuration. This is useful if you're experiencing issues with how certain types of requests are handled.

You can also add additional actions to be performed after the media starts playing, such as:
- Adjusting the volume
- Setting up lighting scenes
- Sending notifications

## Troubleshooting

If your voice commands aren't being interpreted correctly:

1. Check that the script is properly exposed to your voice assistant.
2. Review the LLM prompt settings in the blueprint configuration.
3. Make sure your Spotify Plus integration is working properly by testing direct commands.
4. Check that your media player entity ID is correct.

## Comparison with Voice Intents

This blueprint offers several advantages over traditional voice intents:

- **More natural language processing**: No need to remember exact command phrasing
- **Better context understanding**: LLM can extract multiple parameters from a single request
- **Less overlap**: No issues with overlapping intent patterns
- **More flexible**: Handles a wider variety of request formats

## Credits

- [Home Assistant](https://www.home-assistant.io/) team for the LLM voice capabilities
- [Spotify Plus](https://github.com/thlucas1/homeassistantcomponent_spotifyplus) integration by hokiebrian
- Based on the structure of the [Music Assistant voice script](https://github.com/music-assistant/voice-support) 
