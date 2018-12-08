# Use an existing image ad base image
FROM alpine


# Download and install dependcy
RUN apk add --update redis


# Tell the image what to do when it starts as a container
CMD ["redis-server"]

# Build: docker build -t buzonliao/redis:latest .
# Execute: docker run buzonliao/redis