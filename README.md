# products-api

To run products-api: 
1. Clone the repo and run 'npm i' followed by 'npm run dev' in the root directory of the project, using a terminal such as Git Bash. 
2. The application will be running on localhost:5000/api/products (although it sure won't be pretty if you go there in your browser).
3. To interact with this API, you can use a GUI such as Postman (https://www.postman.com/) - for example, all existing products' entries can be read by sending a GET request to localhost:5000/api/products (with the entries being returned in the response's body). A specific product's entry can be viewed by appending an ID (e.g., 1) on the end of the URL when making the GET request (i.e. to view the product with an ID of 1, send a GET request to localhost:5000/api/products/1). 
4. More CRUD functionality to come. 
