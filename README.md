> MacBubbleBuilder

A macOS alternative to Cimmerian's DaedalusX64 bubble builder.

Credit to Cimmerian for the original bubble-building method and LiveArea structure.

>> Requirements:

	•	Intel Mac running macOS
	
	•	A DaedalusX64 installation on your PS Vita
	
	•	A ROM already copied to your Vita at: ux0:/data/DaedalusX64/Roms/
	
	•	Desired PNGs for your LiveArea icon and background.
No Python, VitaSDK, Homebrew or other development tools are required.

>> Adding a Game

Create a folder inside games/ using the exact name you want to give the bubble.

For example:

	games/
	└── Banjo-Kazooie/
	    ├── raw_icon0.png
	    └── raw_bg.png

The two images must be named:

raw_icon0.png

raw_bg.png

The source images can be any dimensions. MacBubbleBuilder will automatically crop, resize and convert them to the Vita's required formats:
	
		•	icon0.png — 128 × 128, indexed 8-bit PNG
		•	bg.png — 840 × 500, indexed 8-bit PNG
	
The converted images are saved in the game folder.

>> Building a Bubble

Open Terminal and run:

	./build.sh

Enter:

		1	Bubble name — must exactly match the game folder name.
		
		2	ROM name — the filename of the ROM on your Vita. (Not the whole path, just the rom’s filename.)
		
		3	Title ID — exactly 9 uppercase letters/numbers.
		
For the example above:

Bubble name: Banjo-Kazooie

ROM name: Banjo-Kazooie (USA) (Rev 1).z64

Title ID: BANJOKAZO

The builder will create:

Banjo-Kazooie.vpk

Copy the resulting VPK to your Vita and install it with VitaShell. Then restart your device.

>> Image Sources

You will need to find your own suitable icon and background artwork yourself. Save the original images as raw_icon0.png and raw_bg.png in the appropriate game folder.

That's it. The builder handles the conversion, ROM path, SFO generation and VPK packaging automatically.
