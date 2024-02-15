
## Pizzas
Overview
This Pizza Delivery API, built with Flask and SQLAlchemy, serves as a backend system for managing pizzas, restaurants, and the association of pizzas with restaurants including pricing information. It leverages Flask-CORS for cross-origin resource sharing, enabling web applications hosted on different domains to interact with this API.

Features
CRUD Operations: Supports creating, reading, updating, and deleting information about pizzas, restaurants, and their associations.
Relationship Management: Utilizes SQLAlchemy relationships to efficiently manage and query the relationships between pizzas and restaurants.
JSON Responses: Communicates with clients using JSON, making it easy to integrate with front-end applications.
Cross-Origin Requests: Configured with CORS to accept requests from web applications hosted on different origins.
Setup
Prerequisites
Python 3
pip
Installation
Clone this repository or download the source code.
Navigate to the project directory.
Install the required dependencies:
bash
Copy code
pip install Flask Flask-SQLAlchemy Flask-CORS
Initialize the database:
bash
Copy code
flask run
After running the above command, the database app.db will be created and initialized with the necessary tables.

Running the API
To start the API server, run:

bash
Copy code
flask run --port=5555
The API will be accessible at http://localhost:5555/.

Endpoints
GET /pizzas
Retrieves a list of all pizzas, including their id, name, ingredients, and pricing information across different restaurants.

GET /restaurants
Retrieves a list of all restaurants, including their id, name, address, and the pizzas they offer with pricing information.

GET /restaurants/int:restaurant_id
Retrieves details of a specific restaurant by its ID, including the pizzas it offers.

POST /restaurant_pizzas
Creates a new association between a pizza and a restaurant with pricing information. Requires JSON input with pizza_name, restaurant_name, and price.

DELETE /restaurants/int:restaurant_id
Deletes a specific restaurant and its associated pizzas from the data.
Development
This API is developed with Flask, a micro web framework for Python, and uses SQLAlchemy for ORM-based database interactions. It's designed for ease of use and quick integration into web projects requiring a backend for managing pizzas and restaurants.

License
This project is open source and available under the MIT License.
