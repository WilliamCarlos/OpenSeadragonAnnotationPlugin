# Description
- Kind of working image annotation plugin for OSD (feel free to contribute!).

# Getting Started
- Add index.html (which contains the html toolbar/controls) and imageAnnotation.js to your codebase
- Make sure you have all dependencies and their correct verisons (openseadragon, fabricjs, openseadragon-fabricjsOverlay). In this repo for convenience.
- Add your own serialization code if desired. 

# Notes
- If you want to connect these annotations to a database, fill out the createNewSerialization(), updateSerialization(), getAnnotations(), and deleteAnnotation() methods. Commented out Django ajax code is there for reference.
- Otherwise, you can serialize using JSON using the default fabricjs functions
  - JSON.stringify(openseadragon_image_annotations.overlay.fabricCanvas())
  - openseadragon_image_annotations.overlay.fabricCanvas().loadFromJSON([your json])
- The download screenshot button doesn't work (I was doing it server side using PIL, clientside merging not implemented (so if you have some spare time on your hands... ;)
- This is not integrated with the OSD navbar so you'll have to fit in my HTML controls somewhere :/

# Issues
- Serialization. Unfortunately, you'll have to implement most of the serialization yourself if you want to save to a database. Shouldn't be too difficult with my commented code still there, and you can export/import everything using the fabricjs JSON functions mentioned above. 
- If you add css near or around the viewer (i.e. \<br> above the viewer, or add padding left/right of the viewer) the annotations don't scale correctly on zoom. I suspect this is due to the fabric canvas not sticking to the OSD div correctly (this part of the code was taken from https://github.com/altert/OpenseadragonFabricjsOverlay).

# Wishlist <3
- Better textbox UI flow
- Make download button work (clientside, js)
- Rotate annotations on image rotate
- Integrate with OSD controls maybe
- Fix the menu bar css (lost customcss, now it doesn't look as it did in its prime :|)
- Anything else to improve the codebase, I don't have too much time to maintain this but found OSD annotation tools pretty lacking so hopefully this can serve as a starting place for something bigger <3

