# PocketJet 3 Plus setup on Linux

* Extract archive
* Compile drivers
  *     $ cd pocketjet_CUPS
        $ sudo apt install libcups2-dev libcupsimage2 libcupsimage2-dev
        $ ./configure && make
  * If compiling fails with undeclared `stderr` and `stdout` errors, you may need to add `#include <stdio.h>` to `pocketjet.h`.
* Install drivers
  *     $ sudo cp -v rastertopocketjet `cups-config --serverbin`/filter
        $ sudo cp -v *.ppd `cups-config --datadir`/model
* Use printer 
  * Enable bluetooth and scan with blueman-manager
  * Pair with printer (10:00:E8...)
  * Pairing code is `default`
  * Mark device as 'trusted'
  * In settings, add printer by URI (`bluetooth://1000E8...`)
  * Select the driver
  * Restart CUPS
  * Disconnect/reconnect printer
