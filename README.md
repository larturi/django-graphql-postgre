<h1 align="center">
  PoC: FastAPI, GraphQL, PostgreSQL, Docker
</h1>

<h3 align="center">
  -- A simple starter project with FastAPI, GraphQL, PostgreSQL and Docker --
</h3>

<br/><br/>

## 🚀 Quick start

### Create and activate the virtual environment
### `python3 -m venv venv`
### `source venv/bin/activate`

### Create ans start the container
### `docker-compose build`
### `docker-compose up`

<br/><br/>

## 🚀 Panel Postgre Admin
http://127.0.0.1:5050
- admin@admin.com
- admin

### 🚀 Conection in Panel Postgre Admin
- Add new server
- Name: db
- Port: 5432
- User: postgres
- Password: asdf1234$

## 🚀 API GraphQL
http://127.0.0.1:8000/graphql

<br/><br/>

## 🚀 Endpoints

### Create Post
```bash
mutation CreateNewPost {
  createNewPost(
    	title: "FastAPI & GraphQL", 
    	content: "Practicando FastAPI & GraphQL",
    	author: "Leandro"
  ) {
     ok
  }
}
```
### Get All Post
```bash
query {
  allPosts {
    id
    title
    author
    content
  }
}
```
### Find one Post by ID
```bash
query {
  postById(postId: 2) {
    id
    title
    author
    content
  }
}
```

If you have problems with the dependencies:
`pip install fastapi uvicorn sqlalchemy graphene graphene-sqlalchemy alembic psycopg2-binary black python-dotenv`
