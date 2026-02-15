Key design decisions explanation
Why price validation happens at checkout

Because price can change between add-to-cart and checkout  Validating at checkout ensures the user sees the correct price before payment and prevents financial inconsistencies

Why limit total quantity in cart

To prevent abuse, reduce inventory locking issues, and improve logistics plannin

Why use message queue for notifications

Queues allow asynchronous processing, improve system reliability, and prevent blocking core services during high loa

Why microservices architecture

Microservices allow independent scaling, easier maintenance, and separation of responsibilities between domains such as orders, cart, and notifications

Why not send notifications directly from services

Direct calls create tight coupling and reduce reliability. Queue-based communication increases fault tolerance

What happens if push provider is down

Notifications remain in queue and retry mechanism attempts redelivery

Possible improvements

Add notification preferences per user

Add dead letter queue

Add A/B testing for notifications

Add caching layer

Add rate limiting

Edge cases considered

Product removed from catalog while in cart

Price changed during checkout

User logged out

Duplicate notifications

Network failures

Partial failures in services
