FROM nginx:1.21.5-alpine
# RUN \
#   echo '{"status":"UP"}' > /opt/liveness.txt && \
#   echo '{"status":"UP"}' > /opt/readiness.txt

ENV TZ "Asia/Shanghai"

# COPY ./nginx.conf /etc/nginx/
COPY .deploy/default.conf /etc/nginx/conf.d/default.conf

COPY ./dist/index.html /usr/share/nginx/html

ENTRYPOINT ["nginx", "-g", "daemon off;"]
