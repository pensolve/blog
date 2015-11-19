---
layout: post
title: "Finding common spreadsheet errors"
---

Pensolve has release a couple of new features recently to help with finding common spreadsheet errors.

### Hardset numbers
One of the most common spreadsheet errors occurs when formulas contain numbers instead of cell references, known as "hardset values", eg.

= B5 * B6 + 8 * B8

The 8 may represent something physical like their are eight people in your team, which is fine until you add more people to your team.

The inability to quickly see hardset numbers in MS Excel means that these numbers are very difficult to update.

Pensolve helps you find hardset numbers by rendering them in blue in the formula.

![Picture showing hardset number highlighting](/public/2015-11-19/hardset_highlighting.png)

The 0.8 should have been the foundation depth!{: .center-text }

### Inconsistent units

Another major source of errors in engineering calculations is when different magnitudes of units are used. 
While the Pensolve unit analysis tool is still underdevelopment, Pensolve now recognises units that have been input by the user and renders them for the inputs.

When you are inspecting an equation using the equation dependency tracking tool, you can now trace back to the inputs and view the units.

Pensolve also renders the equation using the input values to provide a sanity check that the magnitude of each input is what is expected.

![Picture showing wrong units](/public/2015-11-19/Wrong_units.png)
<p align="center">
  Metres are added to millimetres!
</p>

### Different formulas in an array

Setting up a spreadsheet with this sort of behaviour is asking for trouble. Not only is it difficult to detect when a formula changes within an array, but it is difficult to update the formulas as you need to modify each of the formulas individually.

Pensolve recognises arrays and assesses whether the formulas are the same. 
If the formula is the same it will render the array formula once and place all the outputs in a table. 
If there is a change then two formulas will be produced and two separate shorter arrays are rendered.

![Picture showing different formula in array](/public/2015-11-19/New_array_formula_markedup.png)
<p align="center">
  The formula has changed in the displacement array
</p>
### Incorrect cell reference

When working across multiple sheets it is easy to accidentally reference the wrong cell in an equation.

Pensolve renders the algebraic formula so that you can quickly assess whether the formula is correct.

![Picture showing incorrect reference](/public/2015-11-19/Wrong_cell_ref_markedup.png)
<p align="center">
  mass_1 should have been referenced instead of density!
</p>

### Summary

These new features allow Excel users to quickly find mistakes in their spreadsheets and enforces good spreadsheet calculation practices. The Pensolve team is working hard to develop a robust service that helps engineers eliminate spreadsheet errors, if you think of any new features or improvements then send them in to team@pensolve.com to help us build a useful service for you.

Check out the latest version at [pensolve.com](https://app.pensolve.com).
