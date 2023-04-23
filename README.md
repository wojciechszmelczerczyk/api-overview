# API overview

| Protocol                              | Description                                                                              | Example Use Case                             | Example Request                                                                 | Example Response                                                                               | Format                                    | Type                |
| ------------------------------------- | ---------------------------------------------------------------------------------------- | -------------------------------------------- | ------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- | ----------------------------------------- | ------------------- |
| <p style="color:#6AB344;">REST</p>    | Uses HTTP methods to access resources over the web.                                      | Accessing a blog post.                       | `GET /posts/123`                                                                | `{"id": 123, "title": "Example Post", "content": "This is an example post."}`                  | JSON, XML, HTML, YAML, others             | HTTP, HTTPS         |
| <p style="color:#ffb900">RPC</p>      | Invokes a function or method on a remote server.                                         | Retrieving stock prices.                     | `POST /rpc/get_stock_price` with payload `{"symbol": "AAPL"}`                   | `{"price": 130.21}`                                                                            | JSON, XML, Protocol Buffers, others       | HTTP, HTTPS, others |
| <p style="color:#e10098;">GraphQL</p> | Provides a single endpoint for flexible data queries.                                    | Retrieving a user's profile information.     | `POST /graphql` with payload `{ "query": "{ user(id: 123) { name, email } }" }` | `{"data": { "user": { "name": "John Doe", "email": "johndoe@example.com" } } }`                | JSON                                      | HTTP, HTTPS         |
| <p style="color:#1c1c1c;">CORBA</p>   | Allows distributed objects to communicate with each other across a network.              | Connecting to a remote database.             | `POST /corba/db_connection`                                                     | `{"status": "connected", "session_id": 12345}`                                                 | Binary                                    | TCP/IP, others      |
| <p style="color:#bb0a1e;">SOAP</p>    | Uses XML to exchange structured data between web services.                               | Retrieving weather information.              | `POST /soap/weather` with XML payload                                           | `<WeatherResponse><Temperature>72</Temperature><Condition>Sunny</Condition></WeatherResponse>` | XML                                       | HTTP, HTTPS         |
| <p style="color:#44c767;">RDA</p>     | Provides a standard interface for accessing remote data.                                 | Retrieving sensor data from a remote device. | `GET /rda/sensors/temperature`                                                  | `{"value": 25.5, "unit": "C"}`                                                                 | JSON, XML, others                         | HTTP, HTTPS, others |
| <p style="color:#6ad7e5;">gRPC</p>    | A high-performance, open-source framework for building remote procedure call (RPC) APIs. | Interacting with a distributed system.       | `POST /grpc/GetUserInfo` with Protocol Buffers payload                          | `{"id": 123, "name": "John Doe", "email": "johndoe@example.com"}`                              | Protocol Buffers, others                  | HTTP, HTTPS         |
| <p style="color:#563d7c;">tRPC</p>    | A modern RPC framework with first-class support for TypeScript.                          | Building a distributed e-commerce system.    | `POST /trpc/checkout` with JSON payload                                         | `{"status": "success", "order_id": "ABC123"}`                                                  | JSON, Protocol Buffers, MsgPack, others   | HTTP, HTTPS         |
| <p style="color:#f0b70c;"> AMQP</p>   | A messaging protocol for exchanging messages between applications.                       | Sending and receiving messages.              | `POST /amqp/messages` with AMQP message                                         | `{"message_id": "12345", "content": "Hello World"}`                                            | AMQP, JSON, XML, Protocol Buffers, others | TCP/IP, others      |
