docker build -t packy1014/redis:latest .

# Build from container manually
docker commit -c 'CMD ["redis-server"]' (container-id)