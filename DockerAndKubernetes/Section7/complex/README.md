docker run -it packy1014/frontend npm run test client

# client
docker build -f Dockerfile.dev -t packy1014/client .
docker run -it -p 3000:3000 packy1014/client

# server
docker build -f Dockerfile.dev -t packy1014/server .
docker run -it -p 5000:5000 packy1014/server

# work
docker build -f Dockerfile.dev -t packy1014/worker .
docker run -it packy1014/worker

docker-compose up --build