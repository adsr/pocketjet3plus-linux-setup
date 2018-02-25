# PocketJet 3 Plus setup on Xubuntu 17.10

1. Extract archive

2. Compile drivers

    $ cd pocketjet_CUPS
    $ sudo apt install libcups2-dev libcupsimage2 libcupsimage2-dev
    $ ./configure && make

3. Install drivers

    $ sudo cp rastertopocketjet `cups-config --serverbin`/filter
    $ sudo cp *.ppd `cups-config --datadir`/model

4. Enable bluetooth and scan

5. Pair with printer (10:00:E8...)

6. Pairing code is `default`

7. Mark device as 'trusted'

8. In settings, add printer by uri, `bluetooth://1000E8...`

9. Select the driver

10. Restart CUPS

11. Disconnect/reconnect printer
