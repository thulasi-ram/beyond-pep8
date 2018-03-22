
The Seven Deadly Sins:
1. Lust : overengineering
2. Gluttony : failing to refactor
3. Greed : competing across teams
4. Sloth : not validating inputs
5. Wrath : not commenting code
6. Envy : not using version control
7. Pride : not unit testing

# beyond-pep8
A set of guide lines for people trying out python to think in a pythonic way


1. When initializing an list/dict and populating it inside a for loop..Often there is a way to put it in list comprehension

2. When working with kombu(Celery is built upon kombu) and multi-threaded environment make sure each ThreadConsumer initiates its own connection. Messages received from one connection can only be acked by it. If multiple consumers use same connection and `acks_late` is being used there are chances that same message can be delivered to two or more consumers.
 ref: https://groups.google.com/forum/#!topic/carrot-users/yU7yWZNReyM
 
 

Python Timezone - Django Timezone
Even if your website is available in only one time zone, it's still good practice to store data in UTC in your database. The main reason is Daylight Saving Time (DST). Many countries have a system of DST, where clocks are moved forward in spring and backward in autumn. If you're working in local time, you're likely to encounter errors twice a year, when the transitions happen. (The pytz documentation discusses these issues in greater detail.) This probably doesn't matter for your blog, but it's a problem if you over-bill or under-bill your customers by one hour, twice a year, every year. The solution to this problem is to use UTC in the code and use local time only when interacting with end users.


When a concurrency problem hits you use random sleep. ref: raymond hettinger

Use DDD. Limit db objects to Domain objects. Services should talk with domain objects. That way an api can create a domain object and use the service.

Backends should be a dependency injection to services optionally else it should be picked from config. That way code provides a flexible if two backends are to be used.


Is not java
Pycharm
Less is not always but often better
Lambdas are discouraged - https://www.artima.com/weblogs/viewpost.jsp?thread=147358
Exception handling base exceptions and logging - https://realpython.com/the-most-diabolical-python-antipattern/
Never substitute the behavior of existing package
Use kwargs
Old code is not the Bible
Composition over inheritance
Object bigot and functional programming
Descriptors
Authentication vs authorization
Where to use get and use [] on dictionary 

https://docs.quantifiedcode.com/python-anti-patterns/correctness/assigning_a_lambda_to_a_variable.html

Avoid multiple returns - Multiple exit points for a function is hard to read. But use it if it enhances readablity

Always have returns within try.
Example:
Prefer: try: do xx return except: do yy return than try: do xx except: do yy return.


