# TIL: `Docker Build` Can...

![rw-book-cover](https://pbs.twimg.com/profile_images/744420110832537600/xTIkPdNv.jpg)

## Metadata
- Author: [[@iximiuz on Twitter]]
- Full Title: TIL: `Docker Build` Can...
- Category: #tweets
- URL: https://twitter.com/iximiuz/status/1572149477217079296

## Highlights
- TIL: `docker build` can output an image to a folder 👇
  In particular, it can be used to extract a target image fs w/o running a container:
  ```
  echo 'FROM nginx' > Dockerfile
  docker buildx build -o rootfs .
  ```
  *Requires Docker 18.09+
  Thanks to @GuestChris for the pointer! ([View Tweet](https://twitter.com/iximiuz/status/1572149477217079296))
