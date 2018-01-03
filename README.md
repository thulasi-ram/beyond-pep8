# beyond-pep8
A set of guide lines for people trying out python to think in a pythonic way


1. When initializing an list/dict and populating it inside a for loop..Often there is a way to put it in list comprehension

2. When working with kombu(Celery is built upon kombu) and multi-threaded environment make sure each ThreadConsumer initiates its own connection. Messages received from one connection can only be acked by it. If multiple consumers use same connection and `acks_late` is being used there are chances that same message can be delivered to two or more consumers.
 ref: https://groups.google.com/forum/#!topic/carrot-users/yU7yWZNReyM
 
 
