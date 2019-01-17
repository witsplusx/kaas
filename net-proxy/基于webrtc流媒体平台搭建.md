https://github.com/andyet/SimpleWebRTC
https://github.com/andyet/signalmaster


cd /wits/proj-wkspace/wits-projects-plus

cd signalmaster/
npm install
node server.js
http://localhost:8888/socket.io/


cd SimpleWebRTC/
npm install && npm run test-page

信令

https://github.com/priologic/easyrtc
https://hub.docker.com/r/sylaps/easyrtc-server/

媒体服务器

http://www.kurento.org/

https://hub.docker.com/r/kurento/kurento-media-server/
docker run --rm kurento/kurento-media-server --help
docker run --name kms -p 8886:8888 -d kurento/kurento-media-server

NAT穿透
https://github.com/coturn/coturn

https://hub.docker.com/r/woahbase/alpine-coturn/
https://hub.docker.com/r/kurento/coturn/
https://hub.docker.com/r/2chat/coturn-docker/

https://hub.docker.com/r/zolochevska/turn-server/
https://github.com/anastasiia-zolochevska


VoIP客户端与服务端

https://github.com/versatica/JsSIP
https://github.com/kamailio/kamailio

coturn docker
docker run -d -t --name coturn-single -d -p 3478:3478 -p 3478:3478/udp steppechange/docker-coturn
docker start coturn-single

docker run -d -p 10080:80 -p 17088:7088 -p 18088:8088 -p 18188:8188 efacilitation/docker-janus-webrtc-gateway:latest

docker run --name coturn-sigle coturnbuild:latest


docker run -d  --name coturn-single -p 3478:3478 -p 3478:3478/udp --restart=always zolochevska/turn-server wits wits www.wits.com
docker run -d  --name coturn-single -p 3478:3478 -p 3478:3478/udp zolochevska/turn-server wits wits www.witshine.com


https://bloggeek.me/siganling-protocol-webrtc/
https://docs.traefik.io/

https://xbsoftware.com/blog/free-webrtc-example-with-webix-and-easyrtc/







docker network create --subnet=172.119.0.0/16 net_witshine_dev

docker run -d  --name kms-conturn-svr  -p 3478:3478 -p 3478:3478/udp --network net_witshine_dev --ip 172.119.0.80 zolochevska/turn-server
docker start kms-conturn-svr

docker exec -ti kms-conturn-svr turnadmin -a -b /var/local/turndb -u wits -r kurento.org -p s3cr3t
#kms config
turnURL=wits:s3cr3t@172.119.0.80:3478

docker run --name kms -p 8888:8888 -p 8433:8433 -d --network net_witshine_dev --ip 172.119.0.81 kurento/kurento-media-server:xenial-latest

docker start kms-conturn-svr
docker start kms


http-server -p 8443 -S -C keys/server.crt -K keys/server.key

docker run --name wits-traefik -p 11000:80 -p 11001:8080 -v /wits/proj-wkspace/wits-projects-plus/wits-plusx/AllDocs/docker-images/traefik/traefik.toml:/etc/traefik/traefik.toml -v /var/run/docker.sock:/var/run/docker.sock  -d --network net_witshine_dev --ip 172.119.0.82 traefik





