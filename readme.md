# Description
- Kind of working image annotation plugin for OSD. 

# Notes
- If you want to connect these annotations to a database, fill out the createNewSerialization(), updateSerialization(), getAnnotations(), and deleteAnnotation() methods. Commented out Django ajax code is there for reference.
- Otherwise, you can serialize using JSON using the default fabricjs functions
-- JSON.stringify(openseadragon_image_annotations.overlay.fabricCanvas())
-- openseadragon_image_annotations.overlay.fabricCanvas().loadFromJSON([your json])
- The download screenshot button doesn't work (was doing it server side using PIL, clientside merging not implemented (so if you have some spare time on your hands... ;) ;))
- This is not integrated with the OSD navbar so you'll have to fit in my HTML controls somewhere :/

# Issues
- Serialization. Unfortunately, you'll have to implement most of the serialization yourself if you want to save to a database. Shouldn't be too difficult with my commented code still there, and you can export/import everything using the fabricjs JSON functions mentioned above. 

# Wishlist <3
- Better textbox UI flow
- Make download button work (clientside, js)
- Rotate annotations on image rotate
- Integrate with OSD controls maybe
- Anything else to improve the codebase, I don't have too much time to maintain this but found OSD annotation tools pretty lacking so hopefully this can serve as a starting place for something bigger <3

