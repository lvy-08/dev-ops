# dev-ops

docker container cp Nginx:/etc/nginx/nginx.conf F:/Web/Java/dev-ops/nginx/conf 
docker container cp Nginx:/etc/nginx/conf.d/default.conf F:\Web\Java\dev-ops\nginx\conf\conf.d
docker container cp Nginx:/usr/share/nginx/html/index.html F:\Web\Java\dev-ops\nginx\html

docker run --name Nginx -p 80:80 -v F:/Web/Java/dev-ops/nginx/logs:/var/log/nginx -v F:/Web/Java/dev-ops/nginx/html:/usr/share/nginx/html -v F:/Web/Java/dev-ops/nginx/conf/nginx.conf:/etc/nginx/nginx.conf -v F:/Web/Java/dev-ops/nginx/conf/conf.d:/etc/nginx/conf.d -v F:/Web/Java/dev-ops/nginx/ssl:/etc/nginx/ssl/ --privileged=true --restart=always nginx