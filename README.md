# Serial Date

This peace of code is taken from [this](https://github.com/ludwiggj/CleanCode) repository.
That in its turn is composed from examples of code from the Clean Code by Robert C. Martin.

>“If you go to http://www.jfree.org/jcommon/index.php, you will find the JCommon library. Deep within that library there is a package named org.jfree.date. Within that package there is a class named SerialDate. We are going to explore that class.
The author of SerialDate is David Gilbert. David is clearly an experienced and competent programmer. As we shall see, he shows a significant degree of professionalism and discipline within his code. For all intents and purposes, this is “good code.” And I am going to rip it to pieces.
This is not an activity of malice. Nor do I think that I am so much better than David that I somehow have a right to pass judgment on his code. Indeed, if you were to find some of my code, I’m sure you could find plenty of things to complain about.”

Excerpt From
Clean Code: A Handbook of Agile Software Craftsmanship
Martin, Robert C.
This material may be protected by copyright.

## Why not just use java.utilDate?

> Requirement 1 : match at least what Excel does for dates; Requirement 2 : the date represented by the class is immutable;
> 
> Why not just use java.util.Date? We will, when it makes sense. At times, java.util.Date can be *too* precise - it represents an instant in time, accurate to 1/1000th of a second (with the date itself depending on the time-zone). Sometimes we just want to represent a particular day (e.g. 21 January 2015) without concerning ourselves about the time of day, or the time-zone, or anything else. That's what we've defined SerialDate for.

> You can call getInstance() to get a concrete subclass of SerialDate, without worrying about the exact implementation.

[from the SerialDate javadocs](https://www.jfree.org/jcommon/api/org/jfree/date/SerialDate.html)