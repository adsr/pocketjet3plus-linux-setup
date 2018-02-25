# PocketJet 3 Plus setup on Xubuntu 17.10

Extract archive

Compile drivers

    $ cd pocketjet_CUPS
    $ sudo apt install libcups2-dev libcupsimage2 libcupsimage2-dev
    $ ./configure && make

Install drivers

    $ sudo cp rastertopocketjet `cups-config --serverbin`/filter
    $ sudo cp *.ppd `cups-config --datadir`/model

Enable bluetooth and scan

Pair with printer (10:00:E8...)

Pairing code is `default`

Mark device as 'trusted'

In settings, add printer by uri, `bluetooth://1000E8...`

Select the driver

Restart CUPS

Disconnect/reconnect printer
