# Yatube Blog API
## Project description:
Creating an API for a simplified version of the Yatube blog
The API is implemented for all models of the posts application

__ Available endpoints __

| Endpoints | Method | Description|
|:---:|:----:|:----------:|
| /api/v1/jwt/create/ | POST| getting JWT token|
| /api/v1/jwt/refresh | POST|refresh JWT token|
|/api/v1/jwt/verify/|POST|JWT token validation|
|/api/v1/posts/|POST/GET| Add new post/View all posts|
|/api/v1/posts/{id}/|GET/PUT/PATCH/DELETE|GET/PUT/PATCH/DELETE a post|
|/api/v1/posts/{post_id}/comments/|GET/POST|Getting all comments/Adding a new comment to a post|
|/api/v1/posts/{post_id}/comments/{comment_id}/|GET/PUT/PATCH/DELETE|пGET/PUT/PATCH/DELETE a comment|
|/api/v1/follow/|GET/POST|Getting a list of all subscriptions / New subscription |
| /api/v1/group/|GET|Getting a list of all groups|
|/api/v1/group/{group_id}|GET|getting information about a group|

## Project setup
Clone the repository and change into it on the command line:

`git clone https://github.com/hi-ais/api_final_yatube.git`

`cd api_final_yatube`

Create and activate virtual environment:

`python -m venv env`

`source env/bin/activate`

Install dependencies from requirements.txt file:

`python -m pip install --upgrade pip`

`pip install -r requirements.txt`

Run migrations:

`python manage.py migrate`

Run project:

`python manage.py runserver`

## API request examples
1. Adding a new post to the collection of posts.

```
{
  "text": "string",
  "group": 0
}
```
2. Getting a comment to a post by id.

```
{
  "id": 0,
  "author": "string",
  "text": "string",
  "created": "2019-08-24T14:15:22Z",
  "post": 0
}
```
The full API specification will be available once the project is launched at http://localhost:8000/redoc/.
