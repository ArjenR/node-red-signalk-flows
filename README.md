# node-red-signalk-flows
My nod-red flows for use with SignalK

## ControlDisplay.json
This flow controls display brightness and color for my display using ddcutil. Other displays may work differently or use other adresses. Just use the tool to inspect what is what. ddcui can help to easily try out what would work for a display.

## UPS.json
Flow to read the json report created by the x120x_upsd service and send the information and alerts to SignalK.

## playback_nmea_0183.json
Flow to prune and replay messy nmea sentence logs. It dedupes in batches of one secodn. Can speedup the replay by setting the messages per second.
Uses node-red-contrib-merge-topic

## MOB-tag-processor.json
Works together with bt-sensors-plugin-sk plugin. Will monitor ble-tags or other bluetooth devices where the signal strenght and battery state is set to the sensors.tags.<your_tag_name>.signal and sensors.tags.<your_tag_name>.battery path. Checks every 10 seconds for a lost signal. If this is for 30 seconds it will set the MOB alarm and next waypoint.

TODO: 
- expose signals so parts of the flow can be managed from KIP.
- manage autopilot via api?
