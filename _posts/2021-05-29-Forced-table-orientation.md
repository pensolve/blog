---
layout: post
title: "Manually setting the orientation of a table"
---

Table orientation
-------------------------------------------------------------------

Pensolve uses an algorithm to detect the most likely orientation of a table based
on how equations make use of the data and how the equations are structured within
a table.
However, occasionally it shows an unideal orientation.
While this does not change the final result, it may make things look a bit ugly.

## Manually set table orientation in Pensolve

To address this we have added an option to manually force the orientation of a table.
To do this just add either '-v-' for vertical orientation or '-<>-' for horizontal
orientation in to the cell in the top left above the table (see selected cell in the Figure below).

![Table orientation](http://pensolve.com/blog/public/table-orientation.png){: .center-image }
