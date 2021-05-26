# products-api

To run products-api: 

1. Clone the repo, and in the root directory of the project, first (using a terminal such as Git Bash) install the dependencies: 
```
npm i
```
To start the application: 
```
npm run dev
```
2. The application will be running on localhost:5000/api/products (although it sure won't be pretty if you go there in your browser; also, ensure nothing else is running on that specific port beforehand.)

4. To interact with this API, you can use a GUI such as Postman (https://www.postman.com/) - for example, all existing products' entries can be read by sending a GET request to:
```
localhost:5000/api/products 
```
Upon a successful GET request, all products' entries will be returned in the body of the reponse. 

A specific product's entry can be viewed by appending an ID (e.g., 1) on the end of the URL when making the GET request - i.e. to view the product with an ID of 1, send a GET request to 
```
localhost:5000/api/products/1 
```

5. You can create a new product by making a POST request to localhost:5000/api/products, providing the product's info as a JSON object in the body (raw) of the POST request, like so:

```
{
    "title":"Challenge 31cm Corded Rotary Lawnmower - 1000W",
    "description":"The Challenge electric rotary mower is ideal for grass cutting in smaller gardens. The lightweight design and folding top handle make it easy for      you to use and store. Safety features include a quick stop blade brake and a 2 handed starting switch.",
    "price":50.00
}
```

When successfully created, you will receive a 201 status and the info will be returned to you in the body of the response, along with a randomly-generated ID for the product too. 

6. To update an existing product's entry, send a PUT request to the URL 
```
localhost:5000/api/products/{id}
```
with the ID being the ID of whichever product you wish to edit. 

In the body, include in JSON format the property whose value you wish to update - for example, if you wanted to update the product's price:

```
{
    "price":50.00
}
```
If the request is successful, the product's complete updated details will be returned in the response's body, like so: 
```
{
    "id": "3",
    "description": "Characterized by versatile imaging specs, the Canon EOS 80D further clarifies itself using a pair of robust focusing systems and an intuitive design",
    "price": 50.00
}
```
7. Finally, to delete a product's entry, send a DELETE request to the to the URL 
```
localhost:5000/api/products/{id}
```
with the ID being the ID of whichever product you wish to delete. 

Upon successful deletion, a message containing the deleted product's ID will be returned. 
```
{
    "message": "Product 3 removed"
}
```
