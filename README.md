mkdir adopt && cd adopt &&
git clone https://github.com/trancn-dev/adopt-docker.git &&
git clone https://github.com/trancn-dev/adopt-api.git &&
git clone https://github.com/trancn-dev/adopt-web.git &&
git clone https://github.com/trancn-dev/adpot-cms.git

cd adopt-docker

docker-compose up -d
