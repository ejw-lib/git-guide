# Using Github with Excel Files  

## Overview  
From my understanding, you typically don't use github to store files like Excel.  The reasoning is that github is specifically setup for tracking changes in text files and Excel is a binary file.  

The git version tracking system does a great job of identifying changes occuring on each line of text but due to the format of a binary file, the system tends to save not just the changes but an entire separate copy of the file.  As you can guess, for larger files and repeated changes, the amount of storage space needed increases dramatically.  

Due to these reasons, you can store Excel documents on github as part of a repo but it is adviseable that it is a small file and only small number of changes are made to it.  Often when these files are added to Github then they are done so through the `Releases` option.  This option is used for distributing binary files like software installation files but you could use this section for Excel Binaries also.  Some nice features of the   `Release` area is the abilitlity to add a version number to your document.  This method is more appropriate for binaries than a general repo.  You can still add Excel files to a reposiotry and when cloning there will be no issues but viewing online will not be possible.   

An alternative and suggested way of handling Excel files is to `Save` the Excel file as a `.csv` file.  This is a text format that works well with github.  

A more creative way of storing a complicatd Excel file would be to store the data as a `.csv` file and any `VBA` as a text file (i.e. `.bas`, `.vbs`, or `.txt`).  Next save any formatted spreadsheets without the data and provide instructions for re-assembling the data, VBA, and template spreadsheet in a `README.md`.

