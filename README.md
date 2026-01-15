# Dispatch Decompiling Resources

This repository holds information about decompiling the pak files found in Dispatch.

## Game Version: v1.0.16598

## Required Tools

You will need 3 tools:

1. **FModel** - Browse and extract content from pak files: https://github.com/4sval/FModel
2. **UEAESKeyFinder** - Extract the AES key needed for FModel: https://github.com/EZFNDEV/UEAESKeyFinder
3. **FMod Bank Tools** - Extract audio files: https://github.com/Wouldubeinta/Fmod-Bank-Tools

## Critical Information and Findings

1. The pak files are encrypted and require an AES key for decryption. The key is hard-coded into the `Dispatch\Dispatch\Binaries\Win64\Dispatch-Win64-Shipping.exe` file. You can use a hex editor to extract it manually; UEAESKeyFinder automates this process. Only one key is found and needed.
2. The bank files hold all the audio. These files are not encrypted and can be extracted easily. They are neatly organized and use the standard nomenclature of using DX for dialogue, FX for effects, etc. Audio and video files are linked using their file names.
3. The extracted files take >30GB of space.

## Future Plans

I am working on a simple Python program that uses FFmpeg to combine the audio and video into a single video file. I will be attempting to recreate the game as a visual novel in Unity so I can compile natively for Android (primarily), but other OSes too if required. The script will be posted here.

These resources can help someone who knows more about all this.

The directory structure is visible at https://lxlit.me/Dispatch_Decompiling_Resources/
