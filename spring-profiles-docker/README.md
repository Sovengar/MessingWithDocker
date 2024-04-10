### React Product App using Spring Boot as the backend
![alt text](react-product-app.png)

## Production
`docker-compose up --build -d`
Call localhost:3000

## Development
`docker-compose -f dev-docker-compose.yml up --build -d`
`docker-compose -f dev-docker-compose.yml watch`
Call localhost and localhost/api/products/