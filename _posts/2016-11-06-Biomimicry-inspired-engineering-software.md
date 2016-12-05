---
layout: post
title: "Biomimicry inspired engineering software"
---

The concept of biomimicry is to emulate nature’s time tested processes/strategies to solve human related problems.

The solutions not only tend to provide a very efficient solution but offer an elegance and 
intuitive feel due to their natural roots. I first got interested in biomimicry when I heard 
a [TED talk by Janine Benyus]( https://www.ted.com/talks/janine_benyus_shares_nature_s_designs) who 
talked about how seashells help us design sewage pipes, amongst other things. I then went on to
 read her [fascinating book on the whole movement of Biomimicry]( https://biomimicry.org/janine-benyus/).

When faced with the task of presenting an entire spreadsheet of engineering calculations to the user in an 
intuitive and efficient way for Pensolve, I knew biomimicry would provide me with the solution.

Design problem
--------------

Present the calculations from a spreadsheet (5 to 500+ individual calculations) in a way that allowed the user
to quickly understand how the spreadsheet works and be able to find errors.

Solution – part 1 natural flow
------------------------------

Each of the calculations in a spreadsheet are often inputs for other calculations, which are in turn are
inputs for even more calculations. Essentially the calculations flow from the input cells through a 
series of intermediate calculations to the output cells.

We adopted a flowmap to display the flow of calculations, similar to how a braided river flows. 
Our flowmap goes from inputs on the left to the outputs on the right and allows the user to see how an 
individual calculation affects the outputs and surrounding calculations.

 ![Flow-map like a river](http://pensolve.com/blog/public/flow-map-design.jpg){: .center-image }

Solution - part 2: Overlapping lines
------------------------------------

Turns out that the optimal display of calculation nodes and their connecting lines is a very very difficult 
mathematical problem that sometimes does not have a unique solution. To overcome these issues, we again 
turned to nature to look for solutions. There are many cases in nature where you see branches which are 
somewhat optimises for space (eg. Trees trying to catch sunlight). However, our branches are splitting 
and then re-joining and they often have long connecting lines as well as very short ones.

Our solution was to use physics-based rules to distribute our nodes. We gave all of our nodes a magnetic charge
 so that they would repel each other and provide space. While giving them a gravitational pull towards the
  centre to make sure they didn’t spread out too much. 

We then gave the connecting lines a spring stiffness depending on their length, so that the connected nodes
 would pull closer together. And we assigned a mass to each node and a viscosity to the page, this allowed 
 the user to click and drag a node and it would naturally pull the connected nodes but with a small amount of drag. 

Finally, the nodes were randomly generated on the page and all of the forces would act to bring the nodes to a
natural resting place, which resulted in a semi-optimised layout. The added advantage being that the flowmap 
now has an intuitive/organic feel to it. To achieve this physics based solution above we would like to thank 
the generous efforts of the [contributors to the D3 library]( https://d3js.org).

 ![Sample of flow-map](http://pensolve.com/blog/public/flow-small.png){: .center-image }


Solution – part 3: dealing with different spreadsheet versions
--------------------------------------------------------------

One of the other major challenges with engineering spreadsheets is that engineers tend to create multiple versions
 of a master spreadsheet (e.g. Adding additional calculations for the design of a retaining wall and denoting 
 that spreadsheet to be version two).

While there are probably some magnificent solutions from genetics to work out how the spreadsheet was modified 
and display it to the user, we turned to our backgrounds in seismic engineering. A common site investigation 
technique called cross-hole testing requires the matching of an input signal to a recorded signal, which has 
been modified by travelling through the ground. We converted the calculations in the spreadsheet into a signal 
and through signal matching could map one spreadsheet onto another, even with considerable modifications. 
It is not strictly biomimicry, as the solution is more mathematical, however, the signal modification in cross-hole 
testing is a natural process, so we are still claiming biomimicry here too.

 ![Cross-hole testing](http://pensolve.com/blog/public/cross-hole-testing.png){: .center-image }

[Click here to try out an interactive demo.](https://productionpensolve.blob.core.windows.net/common/flowmap.html?json=aFLOWMAP123.json&json2=bFLOWMAP444.json)

[![displacement-based design example](http://pensolve.com/blog/public/DDBD-flow-map.png)](https://productionpensolve.blob.core.windows.net/common/flowmap.html?json=aFLOWMAP123.json&json2=bFLOWMAP444.json)

Summary
-------

The solution to many design problems both technical and for user experience can be found through nature inspired 
innovation. We found that our biomimicry solutions offered a far more natural user experience and it also made 
it easier to build as we could copy the behaviour that we were so familiar with. I would highly recommend reading 
the book Biomimicry by Janine Belliss, as it is fascinating to hear about the engineering designs that have been 
developed through the process of biomimicry.

More about Pensolve Three
-------------------------

Pensolve Three is the third version of Pensolve, a software solution to manage and review engineering spreadsheets. 
Pensolve converts spreadsheets into hand-written calculations for internal and peer-review. 
It also runs a series of checks on the calculations to assess operational errors. The comparison of spreadsheets 
and understanding master files are the major new features in Pensolve Three. Pensolve is a part of a new group of 
productivity applications for engineers that enhance the engineer rather than automate their work.

Check out this [two-minute summary video.](https://youtu.be/HPXg-4WkhSw)

[![ScreenShot](http://pensolve.com/blog/public/why-purchase-Pensolve.png)](https://youtu.be/HPXg-4WkhSw)


