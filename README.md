
# SUTT Backend Task 1.5 - Django Polls

## About the Project

A basic Django web application where users can view
poll questions, select choices, submit votes and view
voting results.

Administrators can create and manage questions and
choices using Django's built-in admin interface.

## Technologies Used

- Python
- Django
- SQLite
- HTML
- CSS
- Django Debug Toolbar

## Features

- Display recently published questions
- View individual questions
- Submit votes
- Display voting results
- Manage questions and choices through Django admin
- Automated tests
- Debugging using Django Debug Toolbar

## How to Run

1. Clone the repository.

2. Create a virtual environment:

   python -m venv .venv

3. Activate the virtual environment on Windows:

   .\.venv\Scripts\Activate.ps1

4. Install dependencies:

   python -m pip install -r requirements.txt

5. Apply migrations:

   python manage.py migrate

6. Create an administrator account:

   python manage.py createsuperuser

7. Start the development server:

   python manage.py runserver

8. Open http://127.0.0.1:8000/admin/ to create
   questions and choices.

9. Open http://127.0.0.1:8000/polls/ to view polls.

## Running Tests

python manage.py test polls

## Understanding How the Web Works

### 1. What happens when you enter a URL in a browser?

The browser first interprets the URL to determine
the protocol, hostname and requested resource.

If necessary, DNS is used to find the IP address
associated with the hostname.

The browser establishes a connection with the server.
For HTTPS, a secure connection is established.

The browser sends an HTTP request to the server.

The server processes the request and sends an HTTP
response containing the requested resource.

The browser interprets the response, renders the
page and requests additional resources if required.

### 2. What are the client and server?

A client is a device or program that requests
resources or services.

A server receives requests, processes them and
returns responses.

In this project, the browser is the client and
Django handles requests on the development server.

### 3. What is HTTP?

HTTP stands for Hypertext Transfer Protocol.

It defines how clients and servers exchange
requests and responses.

An HTTP request contains a method, request target,
headers and sometimes a body.

An HTTP response contains a status code, headers
and sometimes a body.

### 4. What is the difference between GET and POST?

GET is used to retrieve information from a server.
It should not be used to perform state-changing
operations.

POST submits information to the server for processing
and may change the server's state.

In this project, GET displays a question and POST
submits a vote.

POST does not automatically encrypt data.
HTTPS provides encryption during transmission.

### 5. What do HTTP status codes mean?

200: The request was successful.

302: The browser is redirected to another URL.

404: The requested resource was not found.

500: An unexpected error occurred on the server.

### 6. What are HTML, CSS and JavaScript?

HTML defines the structure and content of a webpage.

CSS controls the appearance and layout of a webpage.

JavaScript allows webpages to perform interactive
operations and respond dynamically to user actions.

### 7. How does a website remember users?

HTTP is stateless, meaning that separate requests
do not automatically remember previous requests.

Cookies are small pieces of information stored
by the browser.

Sessions allow information about a user to be
maintained across multiple requests.

By default, Django stores session data in the
database and uses a session ID stored in a cookie
to identify the session.

### 8. How does a request travel through Django?

Django receives an HTTP request.

Middleware can process the request.

The URL configuration determines which view
should handle the request.

The view executes application logic and may use
models to retrieve or modify database records.

The view can pass data to a template, which
generates HTML.

Django returns an HTTP response to the browser,
passing it through response middleware.

### 9. Why is a CSRF token required?

CSRF stands for Cross-Site Request Forgery.

A malicious website may attempt to make a user's
browser submit an unwanted request to another website.

Django's CSRF protection helps prevent such attacks.

The csrf_token template tag adds a hidden token
to the HTML form.

When the form is submitted, Django validates the
token as part of its CSRF protection.

## Scope

This project follows the official Django Polls
tutorial as required for SUTT Backend Task 1.5.

No additional application features are implemented.
