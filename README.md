# l19-socket.io-message-queue
Message Queue server that monitors database events, and then modifying our API server to fire events into that Queue on all CRUD operations in our models. This uses a 3rd party library (@nmq/q) to do this work.
