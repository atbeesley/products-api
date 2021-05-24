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

4. To interact with this API, you can use a GUI such as Postman (https://www.postman.com/) - for example, all existing products' entries can be read by sending a GET request to localhost:5000/api/products (with the entries being returned in the response's body). A specific product's entry can be viewed by appending an ID (e.g., 1) on the end of the URL when making the GET request (i.e. to view the product with an ID of 1, send a GET request to localhost:5000/api/products/1). 

5. You can create a new product by making a POST request to localhost:5000/api/products, providing the product's info as a JSON object in the body (raw) of the POST request, like so:

```
{
    "title":"Challenge 31cm Corded Rotary Lawnmower - 1000W",
    "description":"The Challenge electric rotary mower is ideal for grass cutting in smaller gardens. The lightweight design and folding top handle make it easy for      you to use and store. Safety features include a quick stop blade brake and a 2 handed starting switch.",
    "price":50.00
}
```

When successfully created, you will receive a 201 status and the info will be returned to you in the body of the response, along with a randomly-generated ID for the product too. 

5. More CRUD functionality to come. 
