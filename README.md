# GIGA Pet Deluxe

Arduino C++ virtual pet project for Arduino GIGA R1 WiFi and the Arduino GIGA Display Shield.

## Download / Arduino IDE usage

The complete sketch is contained in one folder:

```text
GIGA_Pet_Deluxe/
```

To use it:

1. Download or copy the `GIGA_Pet_Deluxe` folder.
2. Open `GIGA_Pet_Deluxe/GIGA_Pet_Deluxe.ino` in the Arduino IDE.
3. Keep all `.h` and `.cpp` files in that same folder so Arduino can compile the sketch.

## Alternative download if binary files are hidden

Some web views do not preview binary `.zip` files. If `GIGA_Pet_Deluxe.zip` is not shown or cannot be downloaded, open the text file:

```text
GIGA_Pet_Deluxe.zip.base64
```

Copy its entire contents into a local file and decode it back to a ZIP archive.

### Linux / macOS

```bash
base64 -d GIGA_Pet_Deluxe.zip.base64 > GIGA_Pet_Deluxe.zip
unzip GIGA_Pet_Deluxe.zip
```

### Windows PowerShell

```powershell
[IO.File]::WriteAllBytes("GIGA_Pet_Deluxe.zip", [Convert]::FromBase64String((Get-Content "GIGA_Pet_Deluxe.zip.base64" -Raw)))
Expand-Archive GIGA_Pet_Deluxe.zip -DestinationPath .
```

Then open `GIGA_Pet_Deluxe/GIGA_Pet_Deluxe.ino` in the Arduino IDE.

## Features

- 480x800 portrait handheld-style UI scaffold with menu, pet home, statistics, shop, inventory, settings, games, and game-over states.
- Object-oriented pet state machine with non-blocking `millis()` animation, stat decay, automatic sleep, random idle actions, and blinking.
- Modular food, shop, inventory, weather, clock, sound, save, and mini-game systems.
- 60 FPS frame scheduler and no `delay()` calls in the main loop.
