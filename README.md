# NASR_2_SCT
THIS BATCH FILE WILL:

1) Pull data from the FAA NASR site and create Sector
   Files (.SCT) for virtual Radar Clients such as
   VRC by MetaCraft. As of now, it will create ALL:
      -Fixes
      -Airports
      -NAVAIDs
      -Airways

2) When appropriate, it will also create an In-Scope
   Reference (ISR) alias (.TXT) file for the data parsed.


NOTES:

 - DME Only stations are placed into the VOR list.

 - All Airways (LOW/HIGH) are placed into the same
   SCT File. Seeing how the intent would never be to
   see all airways at the same time on the scope, but
   rather drawn as needed, it is acceptable to put
   them all under either the HIGH or LOW airways header.

 - This parser can take 10 min or longer to complete.
   Factors such as individual computer performance
   come into play with the duration of this process.

 - This parser utilizes Powershell. Please be sure to
   update to the latest version of Powershell.
