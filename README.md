# node-red-signalk-flows
My nod-red flows for use with SignalK

## ControlDisplay.json
This flow controls display brightness and color for my display using ddcutil. Other displays may work differently or use other adresses. Just use the tool to inspect what is what. ddcui can help to easily try out what would work for a display.

## UPS.json
Flow to read the json report created by the x120x_upsd service and send the information and alerts to SignalK.

## playback_nmea_0183.json
Flow to prune and replay messy nmea sentence logs. It dedupes in batches of one secodn. Can speedup the replay by setting the messages per second.
Uses node-red-contrib-merge-topic
