# Todo
- Figure out why test.js works well but imageAnnotation.js breaks everything when the files are the same?
- Make basic functionality work
- Make download button work (clientside, js)
- Rotate annotations on image rotate
- Change annotation serialization just to JSON (instead of Django ORM)
- Update menubar (some buttons unused)
- Switch from bootstrap to purecss
- Figure out js plugin namespacing
- How to provide menu? Don't really want to integrate with OSD viewer controls... but just giving html is meh
- Figure out how to import/export colors

# In Progress
- Delete color picker ajax stuff
- Colors dictionary -> annotationsJson["strokeColor"]
- Figure out how to deal with importing new/non standard colors (probably make a later feature, when initializing library pass options of colors
- Comment out createNewSerialization (so others can fill in)
- Comment out updateSerialization (so others can fill in)
- Comment out getAnnotations
- Comment out deleteAnnotations
- stroke/strokeColor confusion