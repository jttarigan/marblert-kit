# MarbleRT runner kit (Windows)

MarbleRT is a cross-vendor hardware ray tracing benchmark built for a method paper in preparation. This repository
only hosts the prebuilt Windows kit so that volunteers can run it; the source code and the paper are not public yet.

**Download:** [marblert-windows-2f44fb5c5db5.zip](https://github.com/jttarigan/marblert-kit/raw/main/marblert-windows-2f44fb5c5db5.zip)
(31.8 MB, built from commit `2f44fb5c5db5`)

SHA-256: `faab722a2e7187d9e58e8c045afd84e634352957113a1ef01882a759db3627dc`

## Which GPUs work

The GPU needs hardware ray tracing with Vulkan ray queries:

- NVIDIA GeForce RTX 20 series or newer (desktop or laptop).
- AMD Radeon RX 6000 series or newer, and the AMD integrated Radeon 680M, 760M, 780M or 880M/890M in Ryzen 6000
  and newer laptops.
- Intel Arc discrete cards; the Arc graphics built into Core Ultra processors may work.
- Not supported: Intel UHD / Iris Xe integrated graphics, AMD Vega integrated graphics, GTX cards. The run then
  stops early with an error saying the device has "no ray query support"; nothing is harmed.

A laptop with both an integrated and a discrete GPU uses the discrete one. So far MarbleRT has been run on NVIDIA
only, so results from AMD and Intel GPUs are especially welcome (and may reveal problems: send the console text).

## How to run

1. Download the zip and unzip it to `C:\marblert` (a path without special characters).
2. Laptop: plug in the charger and set the power mode to "Best performance". Desktop: pick the "High performance" or
   "Ultimate Performance" power plan if there is one.
3. Close other applications (browser, games, launchers, Discord, overlays) and set sleep to "Never"
   (Settings, System, Power).
4. Double-click `run_full.bat` (about 1.5 to 2 hours) or, if time is short, `run_short.bat` (about 10 minutes).
   Leave the PC alone while it runs.
5. If Windows SmartScreen says it "protected your PC", choose "More info", then "Run anyway": the program is not
   signed.
6. When the window says "Done", zip the `results` folder inside the kit folder and send it back to the person who
   asked you to run it.

The results contain only measurements and a description of the hardware and operating system (GPU and CPU names,
driver and Windows version, memory size, computer name). Nothing is installed; delete the folder afterwards.
The full guide is `README.md` inside the kit.

## Licenses

MarbleRT: license to be set when the software is deposited with the paper. Third-party components keep their own
licenses: see [THIRD_PARTY_NOTICES.txt](THIRD_PARTY_NOTICES.txt).
