## StupidNice for Android

[![Build Status](https://api.travis-ci.org/StupidNice/StupidNice-android.svg)](https://travis-ci.org/StupidNice/StupidNice-android)
[![Releases](https://img.shields.io/github/downloads/StupidNice/StupidNice-android/total.svg)](https://github.com/StupidNice/StupidNice-android/releases)

A [StupidNice](http://StupidNice.org) client for Android, written in Scala.  
<a href="https://play.google.com/store/apps/details?id=com.github.StupidNice"><img src="https://play.google.com/intl/en_us/badges/images/generic/en-play-badge.png" height="48"></a>


### PREREQUISITES

* JDK 1.8
* SBT 0.13.0+
* Go 1.4+
* Android SDK
  - Build Tools 26+
  - Android Support Repository and Google Repository (see `build.sbt` for version)
  - Android NDK r15+

### BUILD

* Set environment variable `ANDROID_HOME` to `/path/to/android-sdk`
* (optional) Set environment variable `ANDROID_NDK_HOME` to `/path/to/android-ndk` (default: `$ANDROID_HOME/ndk-bundle`)
* Set environment variable `GOROOT_BOOTSTRAP` to `/path/to/go`
* Create your key following the instructions at https://developer.android.com/studio/publish/app-signing.html
* Create `mobile/local.properties` from `mobile/local.properties.example` with your own key information
* Invoke the building like this

```bash
    git submodule update --init --recursive

    # Build the App
    sbt clean go-build android:package-release
```

### TRANSLATE

Translators can go to [POEditor](https://poeditor.com/join/project/u5VHO9vhSf) to help translate StupidNice-android. Guidelines:

* It's okay to leave some strings untranslated if you think it should use the same string as English (US).
* `faq_url` should not be changed. If you'd like to translate FAQ, submit a pull request with the translated [`faq.md`](https://github.com/StupidNice/StupidNice-android/blob/master/.github/faq.md) (it should be named properly, e.g. `.github/faq.zh-CN.md`). Administrators will take care of the rest.
* Do not add/edit/remove comments.

## OPEN SOURCE LICENSES

<ul>
    <li>redsocks: <a href="https://github.com/StupidNice/redsocks/blob/StupidNice-android/README">APL 2.0</a></li>
    <li>mbed TLS: <a href="https://github.com/ARMmbed/mbedtls/blob/development/LICENSE">APL 2.0</a></li>
    <li>libevent: <a href="https://github.com/StupidNice/libevent/blob/master/LICENSE">BSD</a></li>
    <li>tun2socks: <a href="https://github.com/StupidNice/badvpn/blob/StupidNice-android/COPYING">BSD</a></li>
    <li>pcre: <a href="https://android.googlesource.com/platform/external/pcre/+/master/dist2/LICENCE">BSD</a></li>
    <li>libancillary: <a href="https://github.com/StupidNice/libancillary/blob/StupidNice-android/COPYING">BSD</a></li>
    <li>StupidNice-libev: <a href="https://github.com/StupidNice/StupidNice-libev/blob/master/LICENSE">GPLv3</a></li>
    <li>overture: <a href="https://github.com/shawn1m/overture/blob/master/LICENSE">MIT</a></li>
    <li>libev: <a href="https://github.com/StupidNice/libev/blob/master/LICENSE">GPLv2</a></li>
    <li>libsodium: <a href="https://github.com/jedisct1/libsodium/blob/master/LICENSE">ISC</a></li>
    <li>libudns: <a href="https://github.com/StupidNice/libudns/blob/master/COPYING.LGPL">LGPL</a></li>
</ul>

### LICENSE

Copyright (C) 2017 by Max Lv <<max.c.lv@gmail.com>>  
Copyright (C) 2017 by Mygod Studio <<contact-StupidNice-android@mygod.be>>

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program. If not, see <http://www.gnu.org/licenses/>.
