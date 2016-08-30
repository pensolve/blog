---
layout: post
title: "Engineering spreadsheets - Industry statistics"
---

I am impressed and even blown away by the size and complexity of engineering spreadsheets. 
Essentially they are computer software. However, Excel and other spreadsheet software don’t have the same error checking capabilities as modern software languages. 

I started interviewing some engineering firms about how they deal with spreadsheet creation and validation, 
and then found a fantastic study by the Tuck School of Business at Dartmouth College called
[the Spreadsheet Engineering Research Project (SERP)](http://faculty.tuck.dartmouth.edu/images/uploads/faculty/serp/serp_results.pdf){:target="_blank"},
most of the results presented in this article of from that study.

Spreadsheet Size
---------------

It turns out approximately 32% of engineering spreadsheets contain more than 1,000 cells of calculations. 
Pretty serious amounts of time and intellectual property are pumped into these calculations. 

[Include image]

Unfortunately in engineering you are dealing with the real world, 
and often have to modify your spreadsheets to account for particular one-off situations. 
I don’t know about you but reviewing a modified spreadsheet that has 1,000 cells sounds pretty daunting. 

There are simple steps you can take to avoid complete revisions, however, according to the study only 40% 
of engineers would save spreadsheets with a version number and 30% would do nothing for the version control! 

Spreadsheet Documentation
-------------------------

To deal with these large spreadsheets it is a good idea to have some sort of documentation to explain the equations
and the thought process behind the spreadsheet. 
Surprisingly only 7.2% of the 1600 people who took part in the study said they always add documentation
for their spreadsheets either within spreadsheets or in a separate document. 
It is important to develop good practices around spreadsheet documentation or make use
of a [spreadsheet conversion software (eg. Pensolve)](http://pensolve.com?ref=pak_blog){:target="_blank"}, to help build the documentation for you.

Spreadsheets contain errors
---------------------------
Perhaps the biggest problem is not the review time, but the amount of errors in spreadsheets. We are all humans. 
When humans do tasks such as write a line of text or [perform a calculation they are usually 95%-99% accurate](http://panko.com/HumanErr/SimpleNontrivial.html) (depending on how much coffee you have had!). 

That sounds pretty good, but when you have a spreadsheet that connects a few thousand cells together, 
your overall percentage may not be so strong. And unfortunately, self-review seems to have poor results due to two issues. 
First, once you have already looked at the spreadsheet for hours you cannot see the errors that are glaring out at you. 
And secondly, we are fighting a natural self-serving bias that makes us think we are right and therefore not rigorously check for errors.

A good option is to get someone else to review your work, and this is where the documentation comes in really handy. 
The reviewer can not only check your cell-by-cell errors but also understand your design philosophy and check that it is appropriate. 
But before you think this is the silver bullet there is some pretty compelling evidence suggesting that 
[our ability to find spreadsheet errors could be as low as 40%](http://panko.com/ssr/InspectionExperiments.html){:target="_blank"}. 
That means you might need a team to really find those errors. 

Engineering Spreadsheet Protocols
---------------------------------

Because there is a real need to get others to review your work it is really important to implement [best practices around developing 
engineering spreadsheets](https://medium.com/@maxim_52273/the-dos-and-don-ts-of-engineering-spreadsheets-f3a234144f51#.mxf3o1ygu). 
In fact, 85% of engineers share their spreadsheets at least once a month. 
Almost 20% do it every day. 

Implementing a company protocol around spreadsheet formatting makes it easier for others to review 
your work, as they know where to look for different parts of the design process. 
Again, looking at the study results I was surprised to see only 3.4% of organizations have written detailed guidelines and protocols. 
This is certainly an area for improvement.

Summary
-------
There is a saying in software engineering, you spend 10% of your time creating your software and 90% of the time debugging it. 
I think this has to be more at the forefront of engineers minds when they create spreadsheets. 
Make spreadsheets that are simple, make them easier for others to understand, 
and set them up in a logical format that makes them easy to modify and review.
