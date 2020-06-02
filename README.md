# autotypo
Scribus plugin to fix text typography according to french rules...
Adds "add non breaking thin space" before double signs

Specifications inspired from :  https://wiki.openoffice.org/wiki/Non_Breaking_Spaces_Before_Punctuation_In_French_(espaces_ins%C3%A9cables)
- carefull not to change urls as http://etc.usw?so=on
- dont change repeated glyphs as !?!!
- dont change when there is a tab before

# INPUTS
- choose a text frame, launch script
- choose langage
- choose sort of space to add for typography : default is thin nonbreakable space.
- choose whether existing spaces should be replaced or not
# FEATURES
- replaces " with « and » as required
- warns when « and » dont match or for other such issues
- adds choosen spaces after « and before »
- applies some heuristics (some would call that AI) to best deal with ' and "
- when langages is french, does more typography job :
  - replaces or adds the choosen space before ! ? ; : and …
  - doesnt mess urls = doesnt change http://scribus.net
  - only adds one choosen space before a set of double ponctuations as "!!!?!"
# LIMITS
- recognizes urls with "p:/" pattern : it matches http://... but there could be false positive
- same choosen space for « » ; ! ; : …
- space is added or replaced with absolutely no local font awareness
