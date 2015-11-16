Finding common spreadsheet errors
=================================

Pensolve has release a couple of new features recently to help with finding common spreadsheet errors.

### Hardset numbers
One of the most common spreadsheet errors occurs when formulas contain numbers instead of cell references, known as "hardset values", eg.

$$ = B5*B6 + 8*B8$$

The 8 may represent something physical like their are eight people in your team, which is fine until you add more people to your team.

The inability to quickly see hardset numbers in MS Excel means that these numbers are very difficult to update.

Pensolve helps you find hardset numbers by rendering them in blue in the formula.

![Picture showing hardset number highlighting](/public/hardset_highlighting.png)

### Inconsistent units

Another major source of errors in engineering calculations is calculations with different units. 
While the Pensolve unit analysis tool is still underdevelopment, Pensolve now recognises units that have been input by the user and renders them for the inputs.

When you are inspecting an equation using the equation dependency tracking tool, you can now trace back to the inputs and view the units.

Pensolve also renders the input values, to provide a sanity check that the magnitude of each input is what is expected.

### Different formulas in an array

Setting up a spreadsheet with this sort of behaviour is asking for trouble. Not only is it difficult to detect but it is difficult to update the formulas as you need to modify each of the formulas individually.

Pensolve recognises arrays and assesses whether the formulas are the same. 
If the formula is the same it will render the array formula once and place all the outputs in a table. 
If there is a change then two formulas will be produced and two separate tables are rendered.

### Incorrect cell reference

When working across multiple sheets it is easy to accidentally reference the wrong cell in an equation.

Pensolve renders the algebraic formula so that you can quickly assess whether the formula is correct.
