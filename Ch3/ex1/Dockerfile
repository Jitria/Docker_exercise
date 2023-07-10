FROM ubuntu
WORKDIR /usr/share/nginx/html
RUN echo ' <html> \
    <head> \
    <title>Hello!</title> \
    </head> \
    <body> \
    <h1>Hello!! Have a nice day</h1> \
    </body> \
    </html>' > index.html
FROM nginx:latest
COPY --from=0 /usr/share/nginx/html /usr/share/nginx/html
CMD ["nginx", "-g", "daemon off;"]
