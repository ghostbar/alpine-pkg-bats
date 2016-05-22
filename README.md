alpine-pkg-bats
===============

+ **nodejs**: 0.4.0-r0 (`armhf` && `x86_64`)

[More alpine-related stuff here!](https://github.com/ghostbar/alpine-devel)

WHAT IS THIS?
-------------

This is an alternative repository for the latest nodejs packages using alpine
`3.2`, `3.3` and `edge`.

## FAQ

**How do I use it?**

    # echo 'http://ghostbar.github.io/alpine-pkg-bats/v3.2/pkgs' >> \
      /etc/apk/repositories apk --update --allow-untrusted add bats

You could download the package directly as well with:

    $ curl -O \
    https://ghostbar.github.io/alpine-pkg-bats/v3.2/pkgs/x86_64/bats-0.4.0-r0.apk
    # apk add --allow-untrusted bats-0.4.0-r0.apk

**Which way is better to download?**

If you use it in the repo-way then you will always download and install the
latest nodejs. If you decide to download it with curl then you will just use
that version. This is not bad, necessarily, the version will keep existing here,
it won't be deleted if there's a new version packaged, but yet, is an older
version.

**But I'm a crazy person that wants it's docker image as small as possible,
downloading the APKINDEX.tar.gz will bloat it!**

If that's what worries you, then just do a `rm -rf /var/cache/apk/*` and you're
done.

**I'm getting a BAD signature**

You probably changed the name of the package, since the signature is linked to
the package name.

**I'm getting an UNTRUSTED signature**

You need to use `--allow-untrusted` when launching `apk` commands, including
`apk update`.
