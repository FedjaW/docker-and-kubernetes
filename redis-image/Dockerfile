# Use an existing docker image as a base
FROM alpine

# Download and install dependency
RUN apk add --update redis

# Tell the image what to to when it starts as a container
CMD ["redis-server"]