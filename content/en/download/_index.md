---
title: Download
subtitle: Your world is about to change. Welcome to Red.
---

{{< rawhtml >}}

<h2>(*) Extra instructions for Linux and Unix</h2>
<br>
<ul>
    <li>
        For Linux 64-bit distros, you need to install 32-bit supporting libraries. So, for Debian-based distros, install them using:<br>
        <code>sudo apt-get install ia32-libs libc6-i386 libcurl3</code>
    </li><br>
    <li>
        If you are using a Debian 7+ or Ubuntu 13.10+ version, you should use the multiarch way:<br>
        <code>
            dpkg --add-architecture i386<br>
            apt-get update<br>
            apt-get install libc6:i386 libcurl3:i386<br>
        </code>
    </li><br>
    <li>
        For Fedora/Redhat/Centos distros:<br>
        <code>
            sudo yum install glibc.i686<br>
            sudo yum install libcurl.i686<br>
        </code>
    </li><br>
    <li>
        For FreeBSD, no prebuilt binaries yet, you need to cross-compile, or get the Red sources, a Rebol interpreter <a href="http://www.rebol.com/downloads/v278/rebol-core-278-7-2.tar.gz">here</a> and a couple packages: <b>libcrypto.so.8</b>, which can be found in the openssl package, and <b>libcurl.so.4</b> (temporary dependency):<br>
        <code>
            pkg install openssl<br>
            pkg install fpc-libcurl-3.0.2<br>
        </code>
    </li><br>
    <li>
        For ArchLinux, there is a Red package <a href="https://aur.archlinux.org/packages/red/">here</a>.<br>
    </li>
</ul>
<br>

<h2>Install Red using a package manager</h2>
    <ul>
        <li>
            <a href="https://chocolatey.org/packages/red">Chocolatey:&nbsp<code>choco install red</code></a>
        </li>
    </ul>
<br>

<h2>Start Reducing</h2>
    <ul>
        <li>
            Step by step instructions for begining your first project, and compiling your first script can be found <a href="/getting-started/">here</a>.
        </li>
    </ul>

{{< /rawhtml >}}