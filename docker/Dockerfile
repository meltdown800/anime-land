FROM nginx:stable

LABEL maintainer="amiradm"
LABEL version="1.0"
LABEL purpose="anime-site production image"
LABEL environment="production"

# Remove default site
RUN rm -rf /usr/share/nginx/html/*

# Copy my site
COPY html/ /usr/share/nginx/html/

EXPOSE 80
