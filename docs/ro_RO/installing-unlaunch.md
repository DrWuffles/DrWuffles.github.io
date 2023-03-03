---
title: Instalarea Unlaunch
---

::: danger

If you have not yet done so, please follow [Dumping NAND](dumping-nand.html). While the chances are slim, Unlaunch can accidentally brick your Nintendo DSi. A NAND backup + [hardmod](https://wiki.ds-homebrew.com/ds-index/hardmod) would allow you to restore this backup, provided you know how to solder.

:::

::: warning

Make sure your console is charged when following this process. A sudden power loss could result in serious damage.

:::

::: warning

Unlaunch is not compatible with Nintendo DSi development consoles.

:::

## Secțiunea I - Setarea cardului SD

1. Descarcă ultima versiune a [Unlaunch](https://problemkaputt.de/unlaunch.zip)
   - [Link oglindă](https://web.archive.org/web/20201112031436/https://problemkaputt.de/unlaunch.zip), dacă cel de mai sus nu merge
1. Extrage `UNLAUNCH.DSI` din arhiva `unlaunch.zip` și plaseaz-o oriunde pe cardul SD
1. Verifică dacă încă mai ai TWiLight Menu++ pe cardul SD
   - If you are unsure, follow the instructions from the [TWiLight Menu++ install guide](https://wiki.ds-homebrew.com/twilightmenu/installing-dsi)

## Secțiunea II - Instalarea/Actualizarea Unlaunch

1. Deschide TWiLight Menu++
   - If this is your first time installing Unlaunch, relaunch TWiLight Menu++ through the [exploit that you used](launching-the-exploit.html)
   - If you have already installed Unlaunch and are looking to update it, hold <kbd class="face">A</kbd> + <kbd class="face">B</kbd> while booting and select the option labeled `TWiLight Menu++`
   - If several options are labeled `TWiLight Menu++`, select the option in where `BOOT.NDS` is shown at the end of the path on the bottom screen
      - This happens because you are running an older version of TWiLight Menu++, unless you're doing it on purpose, is suggested that you [update your installation](https://wiki.ds-homebrew.com/twilightmenu/updating-dsi)
1. Lansarea Setărilor TWiLight Menu++
   - If you haven't changed your theme, press `SELECT` and touch the small DS icon on the bottom of the touch screen. Altfel, consultă Manualul TWiLight Menu++
1. Apasă <kbd class="l">L</kbd> / <kbd class="r">R</kbd> sau <kbd class="face">X</kbd> / <kbd class="face">Y</kbd> până ajungi la pagina `Setări Unlaunch`
1. Dacă vrei să schimbi imaginea de fundal a Unlaunch, selectează `Fundal`și alege pe cea pe care o vrei
   - Dacă vrei să-ți creezi propriul fundal Unlaunch, vezi [pagina DS-Homebrew Wiki](https://wiki.ds-homebrew.com/twilightmenu/custom-unlaunch-backgrounds)
1. Exit TWiLight Menu++ Settings
1. In the file navigation menu, launch `Unlaunch DSi Installer`
   - If you see two black screens after launching, download [GodMode9i](https://github.com/DS-Homebrew/GodMode9i/releases), put its .dsi file on the SD root, then launch GodMode9i using TWiLight Menu++, and start `Unlaunch.dsi`    
     This method does not enable Unlaunch to use custom patches and background
1. Select the "install now" option
   - If Unlaunch freezes at `ERROR: MISMATCH IN FAT COPIES`, please take a look at the [Troubleshooting](troubleshooting.html) page
1. When completed, reboot your system

If you see Unlaunch's Filemenu screen at this point, you have successfully modded your Nintendo DSi.
- If you see a black screen, please take a look at the [Troubleshooting](troubleshooting.html) page

## Secțiunea III - Configurarea după Instalarea Unlaunch

Currently, Unlaunch defaults to launching its Filemenu on boot, but this can be changed launch whatever you want.

1. Pornește-ți consola în timp ce ții apăsat pe <kbd class="face">A</kbd> și <kbd class="face">B</kbd>
   - Aceasta ar trebui să lanseze Meniul de Fișiere Unlaunch
   - If only the background is shown, or if no files from the SD card are shown (ex. `TWiLight Menu++`), then you'll need to [reformat the SD card](sd-card-setup.html)
1. Navighează la `OPȚIUNI`, și uită-te la opțiunile disponibile
   - <kbd class="face">A</kbd> + <kbd class="face">B</kbd> este hard-codat pentru a lansa în meniul Unlaunch, deci nu poate fi schimbat
   - Opțiunile `NO BUTTON` și `BUTTON A / B / X / Y` pot fi setate cum îți dorești și vor alege ce va lansa pe DSi la pornire în funcție debutoanele care sunt apăsate. Poți selecta orice DSiWare, homebrew, cardul Slot-1, wifiboot, sau Meniul de Fișiere al Unlaunch
      - For TWiLight Menu++, select  `TWiLight Menu++`
      - Pentru Meniul DSi original, selectează `Launcher`
   - `LOAD ERROR` este ceea ce DSi va afișa dacă încarci ceve ce ai setat eșuează, precum faptul că nu ai introdus cardul SD
1. Selectează `SAVE & EXIT` pentru a-ți salva setările, apoi oprește consola DSi

## Secțiunea IV - Curățarea cardului SD

::: tip

This section is optional and only serves for keeping your SD card tidy of files you won't need.

:::

:::: tabs

::: tab name="Memory Pit" default

- Delete the `sd:/private/ds/app/484E494A/pit.bin` file from your SD card
   - If `tip.bin` still exists, then rename it back to `pit.bin`
- You can now restore the `DCIM` folder that was on the root of your SD card, if this folder existed
- Șterge fișierul `UNLAUNCH.DSI` de pe cardul SD

:::

::: tab name="Flipnote Lenny"

- Delete the `800031_104784BAB6B57_000.ppm` and `T00031_1038C2A757B77_000.ppm` files from inside the following folders:
   - `sd:/private/ds/app/4B47554A/001` (Japan)
   - `sd:/private/ds/app/4B475545/001` (USA)
   - `sd:/private/ds/app/4B475556/001` (Europe/Australia)
   - You can also delete the entire folders for the regions besides your own
- Șterge fișierul `UNLAUNCH.DSI` de pe cardul SD

:::
