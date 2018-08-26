=========================
Concurrency in Kombu
=========================

When working with kombu(Celery is built upon kombu) and multi-threaded environment make sure each ThreadConsumer initiates its own connection. Messages received from one connection can only be acked by it. If multiple consumers use same connection and `acks_late` is being used there are chances that same message can be delivered to two or more consumers.

 ref: https://groups.google.com/forum/#!topic/carrot-users/yU7yWZNReyM


