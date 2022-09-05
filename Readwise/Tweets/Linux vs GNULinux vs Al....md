# Linux vs GNU/Linux vs Al...

![rw-book-cover](https://pbs.twimg.com/profile_images/1417581014273122314/2CBEkT0b.jpg)

## Metadata
- Author: [[@iximiuz on Twitter]]
- Full Title: Linux vs GNU/Linux vs Al...
- Category: #tweets
- URL: https://twitter.com/iximiuz/status/1560977903227383810

## Highlights
- Linux vs GNU/Linux vs Alpine Linux 🧵
  1. Linux is the kernel. What Linus wrote in the 90th. That's it.
  Interesting fact: Excluding drivers, the kernel itself is just a few megabytes when compiled. ([View Tweet](https://twitter.com/iximiuz/status/1560977903227383810))
- 2. GNU is a large collection of free software which can be used as an operating system (or in parts with other operating systems).
  You, of course, know this software very well: grep, sed, gcc, the list goes on.
  GNU includes the C standard library implementation called glibc 🔥 ([View Tweet](https://twitter.com/iximiuz/status/1560977904988835842))
- 3. GNU/Linux is any Linux distro (kernel + userland) based on the GNU collection.
  Debian, Ubuntu, CentOS, and even RHEL are technically GNU/Linux.
  Because of the common C stdlib and system tools, often you can jump between GNU/Linux distros w/o much trouble ❤️‍🔥 ([View Tweet](https://twitter.com/iximiuz/status/1560977906628706305))
- 4. Alpine Linux is an alternative Linux distro, not based on the GNU collection.
  Instead of GNU, Alpine uses:
  - BusyBox: a tiny software suite (~2MB) that provides several Unix utilities in a single executable file.
  - musl: a modern and more robust C stdlib implementation 🔥 ([View Tweet](https://twitter.com/iximiuz/status/1560977908793065475))
- 5. Alpine Linux is not a drop-in replacement for GNU/Linux distros like Debian or CentOS!
  musl's behavior may differ from glibc ‼️
  You don't write code in C? It doesn't matter! Unless you use Go, your lang's runtime most likely heavily utilizes the C stdlib provided by the OS. ([View Tweet](https://twitter.com/iximiuz/status/1560977910454001669))
