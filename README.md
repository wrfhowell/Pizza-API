# Pizza-API
For Launch Pad


- An API allows you to interact with a computer or database so that you can easily communicate what information you need or function you want to perform. 
In this case, since the Pizza tracker allow needs to do pretty basic things, I would recommend using a REST API, as they are simple and effective


- A REST api will allow us to perform HTTP methods. THese allow us to send 'GET', 'POST', 'PUT', and 'DELETE' requests to a server via specified URL's. GET will allow us to receive data from the server, POST will allows us to create new information, PUT can change information and DELETE will delete data on the server.


## How the Pizza tracker will use this?
There will be a client side (the app or the website) which will interact to the server holding information about pizza status via a REST API

### Endpoints:
- A customer will need to be able to see what is avaible to order so must send an HTTP "GET" request to '/api/availble-items'. The server will send back a JSON file that the client can parse into an availble menu for the customer to choose from


- A customer will need to be able make an order. This will be an HTTP 'POST' request to '/api/orders' which will create a new order in the server for the restaurant to see


- Note the restaurant will also be able to 'GET' order from '/api/order' to regularly see what new orders they need to make


- Restaurants can use 'PUT' request to '/api/orders/' to change the status from "order-placed" to "being-cooked" to "out-for-delivery"


- Client will continually update with GET to see status of order


- receipt can exist under '/api/receipts/******' with * being replaced with unique order number. can be accessed and changed with http requests


Note, for a more complicated system I would instead recommend using GraphQL subgraphs. GraphQL allows for more specific requests and only one endpoint. This means we can get exactly the data we need with only one request. Opposed to REST which may require multiple requests to different endpoints just to get the data you need (and sometimes extra data that you don't need). BUt since this pizza application is rather simple, a REST api will do just fine.
