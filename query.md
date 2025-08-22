query all books =

>curl localhost:8080/books

add book from json = 

>curl localhost:8080/books --include --header "content-Type: application/json" -d @body.json --request "POST"

query a certain book id = 

>curl localhost:8080/books/1

checkout book = 

>curl localhost:8080/checkout?id=2 --request "PATCH"

return book = 

>curl localhost:8080/return?id=2 --request "PATCH"

