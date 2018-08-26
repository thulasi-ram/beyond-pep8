============================
General rules
============================

#. When initializing an list/dict and populating it inside a for loop..Often there is a way to put it in list comprehension

#. Backends should be a dependency injection to services optionally else it should be picked from config. That way code provides a flexible if two backends are to be used.

#. Python is not Java

#. Always try to have an IDE. (contoversial). My favorite is PyCharm.

#. Less is not always but often better

#. Lambdas are discouraged - https://www.artima.com/weblogs/viewpost.jsp?thread=147358
#. Never substitute the behavior of existing package
#. Use kwargs instead of args
#. Old code is not the Bible
#. Composition over inheritance
#. Object bigot and functional programming
#. Where to use get and use [] on dictionary
#. Avoid multiple returns - Multiple exit points for a function is hard to read. But use it if it enhances readablity
