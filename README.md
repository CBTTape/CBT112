# CBT112
Converted to GitHub via [cbt2git](https://github.com/wizardofzos/cbt2git)

This is still a work in progress. 
Due to amazing work by Alison Zhang and Jake Choi repos are no longer deleted.

```
//***FILE 112 is the source for the TSO command prompter called     *   FILE 112
//*          VTOC.  This file is in IEBUPDTE form.  This command    *   FILE 112
//*          allows you to search the Volume Table Of Contents of   *   FILE 112
//*          one or more disk volumes and obtain listings or totals *   FILE 112
//*          of data sets meeting some criteria.  The specification *   FILE 112
//*          is quite flexible.  This file also contains the HELP   *   FILE 112
//*          data set for this command.   It also contains          *   FILE 112
//*          installation notes, some comments on defaults that may *   FILE 112
//*          not be typical elsewhere,  a list of the known errors  *   FILE 112
//*          in the command,  and ideas for future expansion.       *   FILE 112
//*          This version supports SU60, cataloged datasets and the *   FILE 112
//*          ability to sort the output on anything.  For additional*   FILE 112
//*          changes see the help member of the PDS.                *   FILE 112
//*                                                                 *   FILE 112
//*   >>>>>  Fixed to be EAV compatible with the contributions      *   FILE 112
//*   >>>>>  of Mike Nelson and Dan Dalby.  Older version is        *   FILE 112
//*   >>>>>  obtainable by renaming VTOCCHEO to VTOCCHEK and        *   FILE 112
//*   >>>>>  VTOCEXCO to VTOCEXCP.                                  *   FILE 112
//*                                                                 *   FILE 112
//*   >>>>>  Fix to VTOCCHEK and VTOCFORM from John Gateley to      *   FILE 112
//*   >>>>>  properly find all the extents in EAV volumes.          *   FILE 112
//*                                                                 *   FILE 112
//*          Member $INSTNEW was added to use the ASMA90 (HLASM)    *   FILE 112
//*          assembler, to assemble VTOC.  Please use that member.  *   FILE 112
//*          (Assembled under z/OS 3.1)                             *   FILE 112
//*                                                                 *   FILE 112
//*          Tony Cieri added an option to VTOC of NOTOTALS,        *   FILE 112
//*          which will not produce a TOTALS line.  This seems      *   FILE 112
//*          to have been intended by the author, but an            *   FILE 112
//*          IKJNAME 'NOTOTALS' line needed to be added to the      *   FILE 112
//*          IKJPARS statements.                                    *   FILE 112
//*                                                                 *   FILE 112
//*          A load module for the VTOC command is on File 035      *   FILE 112
//*          and is called VTOC.                                    *   FILE 112
//*                                                                 *   FILE 112
//*          VTOC IS CALLED BY A SUBCOMMAND OF PDS VERSION 8.6      *   FILE 112
//*          FROM FILE 182.  IF YOU HAVE INSTALLED PDS VERSION 8.6  *   FILE 112
//*          YOU SHOULD ALSO INSTALL VTOC.                          *   FILE 112
//*                                                                 *   FILE 112
//*          IF YOU INSTALL PDS VERSION 8.6, SEE THE NOTES IN       *   FILE 112
//*          THIS FILE AS TO WHICH VERSION OF THE VTOCPRNT MODULE   *   FILE 112
//*          YOU SHOULD ASSEMBLE AND LINKEDIT INTO THIS COMMAND.    *   FILE 112
//*                                                                 *   FILE 112
//*          BUGS FIXED, AND SUPPORT ADDED FOR 3390 MODEL 9.        *   FILE 112
//*                                                                 *   FILE 112
//*          YOU SHOULD RE-INSTALL VTOC.    (UPDATED 08-94)         *   FILE 112
//*          FIXED FOR MVS/ESA 5.1.         (UPDATED 07-95)         *   FILE 112
//*          FIXED FOR Y2K SUPPORT.         (UPDATED 12-97)         *   FILE 112
//*          David Spiegel fixes - dyn UCBs (UPDATED 05-99)         *   FILE 112
//*          John Hooper fixes              (UPDATED 07-99)         *   FILE 112
//*          Optional test for DSN enqueues (UPDATED 08-01)         *   FILE 112
//*          MSG macro converted to MSGZ    (UPDATED 08-01)         *   FILE 112
//*          VTOC table now above the line  (UPDATED 08-01)         *   FILE 112
//*                                                                 *   FILE 112
//*           (Thanks also to Seymour Metz.)                        *   FILE 112
//*                                                                 *   FILE 112
//*          ****************************************************   *   FILE 112
//*          * IT APPEARS THAT THERE ARE ADDITIONAL MACROS      *   *   FILE 112
//*          * THAT ARE MISSING FROM THIS FILE  THIS IS IN FACT *   *   FILE 112
//*          * NOT TRUE. WHAT APPEARS TO BE OTHER MACROS WERE   *   *   FILE 112
//*          * JUST AN IDEA AND THOSE MACROS WERE NEVER         *   *   FILE 112
//*          * WRITTEN.  I KNOW ! I SPENT WEEKS TRYING TO TRACK *   *   FILE 112
//*          * THEM DOWN.                                       *   *   FILE 112
//*          *           ARNIE                                  *   *   FILE 112
//*          ****************************************************   *   FILE 112
//*                                                                 *   FILE 112
//* KEYWORDS TSO CP COMMAND PROCESSOR VTOC COMMAND                  *   FILE 112
//*                                                                 *   FILE 112
//*   Note:  The VTOC command processor is called by the LISTV      *   FILE 112
//*          subcommand of PDS Version 8.x (see File 182).          *   FILE 112
//*          If you're installing PDS, then it is very helpful      *   FILE 112
//*          to also install VTOC.                                  *   FILE 112
//*                                                                 *   FILE 112
```
