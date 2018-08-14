in cmd ./Watson call:
node Watson_Inputs_To_Intents.js

MUST HAVE : RabbitMQ Started; MAKE SURE: RabbitMQ HAS A send_to_backend AND A send_to_unity EXCHANGE, and BIND A QUEUE NAMED send_to_backend TO THE EXCHANGE send_to_backend.