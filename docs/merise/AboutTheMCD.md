## Known Limitations & Axes of Improvement

This MCD was designed using AnalyseSI, a Merise 
modeling tool that lacks support for certain data 
types. As a result, some fields appear as DATETIME 
instead of the more appropriate INT or TIME types.

From an optimization standpoint, storing time values 
as integers (minutes since midnight) would have been 
preferable, as it offers better memory efficiency and 
reduces time complexity for the scheduling algorithm 
that will be implemented in the backend.

This limitation will be addressed at the SQL 
implementation stage, where the correct data types 
will be applied. A utility layer in the backend will 
handle the conversion between integer values and 
human-readable time formats (e.g., 510 → "08:30"), 
ensuring consistency across the entire system.
