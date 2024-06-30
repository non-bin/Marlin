# Notes

- Keep belts tight
- Try not to touch the print bed, the oils on your skin can affect adhesion
  - Clean with soap and water, or isopropyl alcohol if you don't have time
- Keep filament in a plastic bag with a desiccant pack when you're not using it
- When changing nozels
  - Heat the hotend and remove the filament
  - Remove the previous nozel
  - Back out the bowden tube
  - Screw the new one in but not all the way
  - Push the bowden tube back in and secure
  - Finish tightening the nozel

## Main Board

- Edit `Marlin/Configuration.h` and `Marlin/Configuration_adv.h` to configure the firmware
- Use VSCode with `PlatformIO` and `Auto Build Marlin` extension
- Open ABM from the left panel, and click `Show ABM Panel`
- Click `Build` next to `STM32F103RE_creality_xfer (512k)`
- Copy `.pio\build\STM32F103RE_creality_xfer\firmware-XXXXXXX-XXXXXXX.bin` to the SD card
- Delete any other `.bin` files
- Power off and completly unplug the printer
- Insert the SD card into the main SD slot
- Power on the printer

Config was based off `https://github.com/MarlinFirmware/Configurations/tree/release-2.1.2.4/config/examples/Creality/Ender-3%20V2/CrealityV422/MarlinUI` at `401c149` on Jun 22, 2024

*RE or RC are two different versions of the STM32F103 chip, which dictate the 256/512 firmware size, and you have an RE. standard is standard, xfer enables USB update support (which I can't make work), and Maple is depricated.

Firmware last updated to `a942c9` on Jun 22, 2024

## Display

- `https://github.com/MarlinFirmware/Configurations/`
- Scroll down to `Release Branches` and click `Download Zip` on the latest release
- Navigate to `/config/examples/Creality/Ender-3 V2/LCD Files/`
- Copy the `DWIN_SET` folder to the root of the SD card
- Power off and completly unplug the printer
- Unplug and remove the display, then remove the back cover
- Insert the SD into the slot on the back of the display board
- Plug the display back in and power on the printer (don't reassemble the back cover yet)
- The LCD should switch from a blue to an orange blank screen
- Wait about a minute on the orange LCD screen (just to be safe)
- Power off the printer
- Remove the microSD card from the LCD’s circuit board, and power on your printer again
- The LCD should now load your firmware’s new home screen
- NOW reassemble the back cover and you're done

Last updated to `6cce77b` on Jun 22, 2024
