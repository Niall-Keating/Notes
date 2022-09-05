# What Is a Distroless Con...

![rw-book-cover](https://pbs.twimg.com/profile_images/1417581014273122314/2CBEkT0b.jpg)

## Metadata
- Author: [[@iximiuz on Twitter]]
- Full Title: What Is a Distroless Con...
- Category: #tweets
- URL: https://twitter.com/iximiuz/status/1566827552781524995

## Highlights
- What Is a Distroless Container Image? 🧵
  Go (programming language) is famous for its statically linked binaries. You can take a Go executable, drop it into a "FROM scratch" container, and call it a day.
  But there might be a problem (keep reading) 👇 
  ![](https://pbs.twimg.com/media/Fb53yR-XoAMfb_U.png) ([View Tweet](https://twitter.com/iximiuz/status/1566827552781524995))
- 1. "FROM scratch" containers lack proper user management.
  The "scratch" base image means an empty image. So, the `/etc/passwd` and `/etc/group` files are simply missing.
  Most of the time, it makes the containerized process run as root. ([View Tweet](https://twitter.com/iximiuz/status/1566827555260223488))
- 2. "FROM scratch" containers lack some much-needed folders.
  `/tmp, /root, /home, /var, /etc` - non of them exist in the scratch container (unless you mount some of them, of course).
  But that can make our programs faulty - just try creating a tmp file and see what happens 😉 ([View Tweet](https://twitter.com/iximiuz/status/1566827557047107585))
- 3. "FROM scratch" containers lack CA certificates and timezone information.
  Calling an HTTPS endpoint? Impossible.
  Doing time conversion? Impossible. ([View Tweet](https://twitter.com/iximiuz/status/1566827558804639744))
- 4. "FROM scratch" containers lack your language runtime.
  If your language's static linking support is less perfect than Go's or your programs require an interpreter or a runtime environment, you can barely use scratch containers. ([View Tweet](https://twitter.com/iximiuz/status/1566827560561934336))
- 5. GoogleContainerTools/distroless images exist to solve the above problems.
  - distroless/static = scratch + a distro-like directory structure, /etc/{passwd,group}, CA certs, and timezones
  - distroless/base = distroless/static + glibc
  - distroless/cc = distroless/base + libgcc ([View Tweet](https://twitter.com/iximiuz/status/1566827562193616898))
- 6. There are also language-specific distroless images:
  - distroless/java for Java 11 & 17
  - distroless/nodejs for Node.js 14 & 16 & 18
  - distroless/python3, well, for Python 3 (but it's still experimental). ([View Tweet](https://twitter.com/iximiuz/status/1566827563942645760))
- 7. Who uses distroless images:
  - Kubernetes (for its service containers)
  - Kubebuilder (for the operator's deployment)
  - Knative
  - Jib and ko!
  If you build your app using Jib or ko, you're also a (happy?) distroless user. ([View Tweet](https://twitter.com/iximiuz/status/1566827565670612993))
- Read more about distroless images in my recent write-up 🔽
  https://t.co/1t6fSLQEcA ([View Tweet](https://twitter.com/iximiuz/status/1566827567184842752))
- Traditional reminder: There is a way to get all my future write-ups right into your inbox 😉
  https://t.co/Fne4AemHIm ([View Tweet](https://twitter.com/iximiuz/status/1566875750644465664))
