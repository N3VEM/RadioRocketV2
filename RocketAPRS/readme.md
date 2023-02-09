##APRS in the Rocket

### Bill of Materials for APRS in the Rocket
* [lightAPRS-W 2.0](https://www.qrp-labs.com/lightaprsw2.html).
* Materials of your choice for building the sled to hold it (I used some bits of perf board for mine)
* 9v Battery and terminal for powering the tracker.
* [SMA edge connectors](https://amzn.to/3HIC7rE)

### Physical Construction
Use a hole saw of the proper diamater to cut the ends of the sled to the desired size, to fit inside your body tube. if you don't have the exact size needed, use one size larger, then put a bolt through the middle, clamp the bolt into your drill chuck, and use the drill to spin the disks against a peice of sandpaper until they are sanded down to the needed diamater.  
     
Cut the slot that supports the battery, and the notches on the side of the sled that will prevent the zip ties from sliding around. I did this cutting with a [pair of nibblers](https://amzn.to/3xcUHmM), but careful use of a dremel tool should do the job as well.  
     
Use the tracker to mark the hole locations to attach the tracker to the sled, and drill out holes that will fit M2 hardward.
     
Solder the 9v Battery leads to the + and - power connections on the tracker.
     
Solder SMA edge connectors onto the antenna connections on the tracker board.
     
Mount the tracker to the sled using M2 hardward.
     
Using the main part of the sled with the mounted tracker as a guide, mark the location that the sma connectors hit the round end piece, and drill holes so that they will slide through.  The SMA hardware will support this sled end-cap.
     
Use super glue to tack and hold the other end in position, and then add epoxy fillets at the corners to strengthen the bond.
     
*DO NOT* connect the batter or power up the tracker before programming and attaching antennas.

### Software
* Set up will be done primarily using the information available on the [lightAPRS-W 2.0 github page.](https://github.com/lightaprs/LightAPRS-W-2.0).
* After all the directions there are completed (ensuring that you've copied the proper libraries etc. as is described in those directions), you can use the .ino file located here, instead of the 'factory default'.  Just be certain to modify the code with information like your own callsign, where noted (Don't use my callsign!)
     * .ino file will be uploaded here after some initial testing.   I don't want to upload code that might damage your equipment before testing it on my own :-)
