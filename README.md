In order to get a Chrome build with Flash, run the following commands on Linux (to install linux on chromeos, you will need a supported chromebook check in settings)

This downloads the Ungoogled Chromium build
```
wget https://github.com/systeminbits/ungoogled-chromium-binaries/releases/download/87.0.4280.141-1.1/ungoogled-chromium_87.0.4280.141-1.1_linux.AppImage
```
This makes Ungoogled Chromium an executable to run.
```
chmod +x ungoogled-chromium_87.0.4280.141-1.1_linux.AppImage
```
This downloads Flash Player
```
wget https://github.com/2Epik4u/flash-player-linux/raw/main/flashbuilds/linux/64%20bit/libpepflashplayer.so
```
This runs Ungoogled Chromium with Flash Player loaded, and disables the sandbox (disabling sandbox is needed or else websites wont load)
```
./ungoogled-chromium_87.0.4280.141-1.1_linux.AppImage --no-sandbox --ppapi-flash-path=libpepflashplayer.so --allow-outdated-plugins
```

Now, paste ``chrome://settings/content/siteDetails?site=https%3A%2F%2Fflashthemes.net`` in the addresss bar, and click allow flash.