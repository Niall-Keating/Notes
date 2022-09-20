# Tweets From Ivan Velichko

![rw-book-cover](https://pbs.twimg.com/profile_images/1417581014273122314/2CBEkT0b.jpg)

## Metadata
- Author: [[@iximiuz on Twitter]]
- Full Title: Tweets From Ivan Velichko
- Category: #tweets
- URL: https://twitter.com/iximiuz

## Highlights
- TIL: `docker build` can output an image to a folder 👇
  In particular, it can be used to extract a target image fs w/o running a container:
  ```
  echo 'FROM nginx' > Dockerfile
  docker buildx build -o rootfs .
  ```
  *Requires Docker 18.09+
  Thanks to @GuestChris for the pointer! ([View Tweet](https://twitter.com/iximiuz/status/1572149477217079296))
