   



// normal docker compose
docker-compose -f .\numbers\docker-compose.yml up -d
docker-compose -f .\todo-list\docker-compose.yml up -d


// override file
// seeing the join file without actually deploying
docker-compose -f ./todo-list/docker-compose.yml -f ./todo-list/docker-compose-v2.yml config

// deploying
docker-compose -f ./numbers/docker-compose.yml -f ./numbers/docker-compose-dev.yml -p numbers-dev up -d
docker-compose -f ./numbers/docker-compose.yml -f ./numbers/docker-compose-test.yml -p numbers-test up -d
docker-compose -f ./numbers/docker-compose.yml -f ./numbers/docker-compose-uat.yml -p numbers-uat up -d

docker-compose -f ./numbers/docker-compose.yml -f ./numbers/docker-compose-uat.yml -p numbers-uat down












































