# Webpack optimization

docker build -f Dockerfile.webpack -t portfolio_webpack .
docker run --name portfolio_webpack_container -p 8080:8080 -v ./optimized:/app/optimized -d portfolio_webpack

sudo docker exec -it portfolio_webpack_container sh
npx webpack

sudo docker stop portfolio_webpack_container
sudo docker rm portfolio_webpack_container
sudo docker rmi portfolio_webpack