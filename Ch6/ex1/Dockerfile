FROM ubuntu:latest
RUN apt-get update && apt-get install -y -q nginx && apt-get install -y curl
COPY index.html /usr/share/nginx/html
HEALTHCHECK --interval=10s --timeout=3s CMD curl -f http://localhost/ || exit 1
CMD ["nginx", "-g", "daemon off;"]
