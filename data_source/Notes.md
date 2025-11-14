SELECTEDVALUE() 
- checks filter context, not row context
- if a slicer is selecting a single value, then SELECTEDVALUE() works and gives the value selected by the slicer
- a bar chart with countries in the x-axis will create row context and not filter context. Hence, SELECTEDVALUE() will not work
- MAX() is a better way to check which is the row

