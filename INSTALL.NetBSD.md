How to Install Open vSwitch on NetBSD
=====================================

On NetBSD, you might want to install requirements from pkgsrc.
In that case, you need at least the following packages.

  * automake
  * libtool-base
  * gmake
  * python27
  * py27-xml
  * pkg_alternatives

Some components have additional requirements. (See [INSTALL.md])

Assuming you are running NetBSD/amd64 6.1.2, you can download and
install pre-built binary packages as the following.
(You might get some warnings about minor version mismatch.  Don't care.)

    ```
    # PKG_PATH=http://ftp.netbsd.org/pub/pkgsrc/packages/NetBSD/amd64/6.1.2/All/
    # export PKG_PATH
    # pkg_add automake libtool-base gmake python27 py27-xml pkg_alternatives
    ```

NetBSD's `/usr/bin/make` is not GNU make.  GNU make is installed as
`/usr/pkg/bin/gmake` by the above mentioned `gmake` package.

As all executables installed with pkgsrc are placed in `/usr/pkg/bin/`
directory, it might be a good idea to add it to your PATH.

Open vSwitch on NetBSD is currently "userspace switch" implementation
in the sense described in [INSTALL.userspace.md] and [PORTING.md].

[INSTALL.md]:INSTALL.md
[INSTALL.userspace.md]:INSTALL.userspace.md
[PORTING.md]:PORTING.md
