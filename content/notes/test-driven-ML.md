---
Title: Test Driven Development for Machine Learning
---

## Test Driven Development 

Test driven development is a concept for writing software in which a developer doesn't write any production code prior to writing the unit tests for said production code.  Instead of trying to fix bugs and rewrtie code after the fact, the production code from the start is written to past the predetermined tests. While not a typical practice in machine learning, I think it is especially valuable in modern ML including novel implemenations as well as pipelines that can include many stages of transformation.  Not only valuable for those writing production ML code, but can be useful for those during the learning process of advanced ML concepts.  For me personally, one issue I have run into when using new code or model arhcitectures I was learning, was a strugle to find the source of errors due to my incomplete understanding of what was happening in the code.  In most cases this was merely a data or shape transformation I wasn't paying attention to.  

An example in which test driven development would be beneficial during the learning process is to instead of just going straight into writing the code, consider what happens throughout the process, determine every point in which an action takes place, and then write a test to determine whether the action happens in the way it is expected to.  This includes early steps like data loading, imediately check for data types and expected amount of data.  During transformation stages, check for matrix dimensions before and after transforms. One of the most useful areas for implementing unit testing in ML is cases that don't result in an error, but still fall outside of the expected output. Determine the expected range of output values whether thats values between 0 to 1 or -1 to 1 and make sure your outputs are within the range. The process of test driven development forces one to think more deeply about the coding process which is important when implementing methods that are new to you, while also ensuring the final implementation is much less error and bug prone.   