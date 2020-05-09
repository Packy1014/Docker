npx create-react-app frontend

docker build -f Dockerfile.dev -t packy1014/frontend:latest .

docker run -it -p 3000:3000 -v /app/node_modules -v $(pwd):/app packy1014/frontend

docker-compose up --build

docker-compose down

docker run -it packy1014/frontend npm run test

docker exec -it CONTAINER_ID sh
docker attach CONTAINER_ID

docker build -t packy1014/frontend-nginx:latest .
docker run -p 8080:80 packy1014/frontend-nginx:latest