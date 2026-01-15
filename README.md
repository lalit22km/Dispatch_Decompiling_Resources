# Dispatch Decompiling Resources

This repository holds information about decompiling the pak files found in Dispatch.

### Game Version : v1.0.16598

You will need 3 tools :

1. FModel to browse and extract the content in the pak files : https://github.com/4sval/FModel
2. UEAESKeyFinder to extract the AES key needed in FModel : https://github.com/EZFNDEV/UEAESKeyFinder
3. FMod Bank Tools to extract the audio files : https://github.com/Wouldubeinta/Fmod-Bank-Tools

### Critical information and findings

1. The pak files are encrypted and require the AES key for decryption. The key is hard coded into the "Dispatch\Dispatch\Binaries\Win64\Dispatch-Win64-Shipping.exe" file. You can use a hex editor to extract it manually, UEAESKeyFinder automates that process. Only one key is found and needed.
2. The bank files hold all the audio. These files are not encrypted and can be extracted easily. They are neatly organised and use the standard nomenclature of using DX for dialogue, FX for effects etc. Audio and Video files are linked using their file names.
3. The extracted files take up more than

### Future plans

I am working on a simply python program that uses ffmpeg to combine the audio and video into a single video file because I will be attempting to recreate the game as a visual novel in Unity so I can compile natively for Android mainly but other OSes too if required. The script will be posted here.

These resources can help someone who knows more aobut all this.

The directory structure is visible at
