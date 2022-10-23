## About the project
This project is a simple web server create to absorb the content and studies from golang programming language

### API docs

* `http://localhost:8000/movies` get all movies METHOD(GET).
* `http://localhost:8000/movies` create a movie `the object type to send to api it's the type Movie` METHOD(POST).
* `http://localhost:8000/movies/{id}` get a movie by id METHOD(GET).
* `http://localhost:8000/movies/{id}` delete a spcecific movie METHOD(DELETE) 
* `http://localhost:8000/movies/{id}` update a spcecific movie METHOD(PUT).

### JSON OBJECT FORMAT

```
type Movie struct {
	ID       string    `json:"id"`
	Isbn     string    `json:"isbn"`
	Title    string    `json:"title"`
	Director *Director `json:"director"`
}

type Director struct {
	Firstname string `json:"firstname"`
	Lastname  string `json:"lastname"`
}
```

### EXAMPLE
```json
{
	"isbn": "438227",
	"title": "Movie One",
	"director": {
		"firstname": "John",
		"lastname": "Doe"
	}
}

```


## Getting started

to run this project you need to clone this repository and use the `go run main.go` command in your CL shell

### Layout

```tree
├── static
├── main.go
└── README.md
```

A brief description of the layout:

* `main.go` the api entry point
