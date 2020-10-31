# NASR_2_SCT
THIS BATCH FILE WILL:

1) Pull data from the FAA NASR site and create Sector
   Files (.SCT) for virtual Radar Clients such as
   VRC by MetaCraft. As of now, it will create ALL: Fixes, Airports, NAVAIDs, & Airways.

2) When appropriate, it will also create an In-Scope
   Reference (ISR) alias (.TXT) file for the data parsed.


NOTES:

 - DME Only stations are placed into the VOR list.

 - All Airways (LOW/HIGH) are placed into the same
   SCT File with a header of "HIGH AIRWAY".
   Seeing how the intent would never be to
   see all airways at the same time on the scope, but
   rather drawn as needed, it is acceptable to put
   them all under either the HIGH or LOW airways header.

 - This parser can take 10 min or longer to complete.
   Factors such as individual computer performance
   come into play with the duration of this process.


KNOWN ISSUES:

 - The NAV ISR (.NAV*) will sometimes have a duplicate entry
   due to the FAA sometimes having the same VOR ID as an NDB ID.
   In this case, the clients like VRC will only pick up and
   display the first command that it finds which may not always be
   the NAVAID you were wanting. This is rare.
   
 - If the longitude has an "East" designation, VRC will draw these
   points on the right side of the display due to a limitation with
   how VRC handles points to the left of the Antimeridian Line (W/E 180.00.00.000).
   We have developed a converter to allow these points to be
   repositioned to the left side of the display by "Tricking" VRC
   but the full implementation for this process is a WIP.


REQUIREMENTS:

 - This BATCH File Requires Powershell v3 or higher. v5.1 or later is recommended.
   You may update Powershell by downloading the Windows Management Framework:
   https://www.microsoft.com/en-us/download/details.aspx?id=54616echo.

 - If your selected "Project Folder" already has previously
   output files in it, be sure to remove these or rename
   them prior to running the BATCH File again.
