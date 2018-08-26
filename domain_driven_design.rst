=========================
Domain Driven Design
=========================

- Use nouns for entities and verbs for services

- Limit db objects to Domain objects. Services should talk with domain objects. That way an api can create a domain object and use the service.

- An domain should not contain only an id reference to another domain. They should not be travesable from on to another. Eg: booking and hotel are domains. One should not be able to access hotel from booking.hotel instead booking should hold the reference for hotel which is hotel_id.


