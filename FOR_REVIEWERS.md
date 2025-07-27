Hi. This will be super quick, but I would like you to take these in mind when reviewing the CAD model.

**MAJOR NOTE: Please read the journal in its entirety before reviewing the model! There are a few things explained as context for the model.**

# Major "issues" you may come across

- **The part cooling fans need to be screwed in after being slid on**
  - I don't really have a big solution for this. For now, it is what it is and it can be changed at any time after approval. I believe that a solution can be implemented in the future as it is not a required feature of the printer.
- **The GT2 belts are too big on the gantry and are clipping with its neighbors**
  - This is due to a fault in sourcing CAD files. The [real listing](https://www.aliexpress.com/item/1005007557987612.html)'s height is 8.5mm and the CAD model is 10mm tall.
- **There are no mounting guides for the gantry motors**
  - You may see this if you're looking at the STEP file. The mounting guides aren't in the final assembly, they're in the "Nema Mount Guides" folder in the OnShape document.
- **The PSU mount isn't secured on the other side**
  - I planned for the electronics box to be printable in one body, and going further than the box itself wouldn't be printable. I could technically add a bracket between the box and the PSU at the screw hole but it would not solve the PSU's ability to move. I could add two screws to secure the supply, but the screw was designed to guide the PSU next to the electronic box, not to secure it.

# Minor Issues

I would prefer to be notified about minor issues (e.g. printability concerns) instead of the project being rejected. CAD files can be altered but as an unemployed student, losing 350 USD is considerably unfavourable, particularly if the reason for rejection is minor. 

By the way, the error in the gantry is from a group mate which allows me to move the gantry (the mates are in order, but it seems that some don't connect well). Additionally, the male t-plug connector will utilise 0.8mm wafer head screws due to the tight real estate (the part cooling part will house a threaded insert for the plug to be screwed into).

# BOM Differences
- I use 200mm linear guides in the BOM as they're cheaper and work the same as 300mm rails (build area is only 180x180)