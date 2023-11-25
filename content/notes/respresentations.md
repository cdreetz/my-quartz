---
Title: Representations and Relationships
---


Modern machine learning is seemingly more and more complex and harder to understand for a lot of people.  Yet the general idea of what happens in every system, no matter how state of the art it is, remains the same.  Progressing machine learning techniques are either new ways to represent data or new ways to determine relationships between data.  Ways to represent images, videos, words, or entire languages.  Relationships between pixels or features within images, or the relationship between each word in a vocabulary.  New systems just learn in cases that part of an image looks like this, the rest of it is usually this.  Or when someone says this, it is usually followed by this.


People have no definitve way of measuring the relationship between colors, naturally.  A person might know yellow is similar to orange, and purple is similar to blue, but theres no way to say how similar. Let's consider the colors of the rainbow in order [ R O Y G B I V ], and lets just represent them by the number they are in that order, so red = 1 and yellow = 3.  Now lets say a the difference between a color and itself is 0, and that larger the difference between colors the further away from 0 it is.  Even though we can't really determine how similar red is to yellow, we know that 1 is 2 values away from 3, or that the difference between red and yellow is -2.  

Now let's think of someone who can't see, but they understand numbers.  If shown the color red and the color yellow, they have no way to determine if they are similar or not, but if you tell them that they are 2 colors away from eachother, on a scale of 7 colors, they can suddently understand exactly how similar the two colors are without ever seeing them.  A computer doesn't know how similar colors are, but it knows the difference between values, and it can find these differences in huge volumes.


This same concept can be applied to many different mediums, it's just a matter of how well humans figure out a way to represent these things in a way that can be measured.  Once p 