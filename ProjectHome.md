PHP 5.2.17 is no longer supported by [PHP developers](http://php.net) team and therefore in the repository we will add security patches and various fixes for it. Oldstable PHP version (5.2) is not compatible with new development version (5.3, 5.4), but it is need for many older applications, we use it on web hosting service for our customers, it is especially popular in Russia and CIS countries.

Patches and fixes was taken from various free sources. We were getting patches from centos.alt.ru repository, from Debian patches and from PHP svn trunk.

Make more secure your server with our security patch. Use our project for download the last version of PHP 5.2.17+ with security and bugfix patches.

Also we have added [our patches](http://code.google.com/p/php52-backports/downloads/list?can=1) into FreeBSD [lang/php52](http://www.freshports.org/lang/php52) port.

Download the last version of the source code with all patches (maybe is not stable, please test this and write to [Issues list](http://code.google.com/p/php52-backports/issues/list) if any problem exist):
> <pre>svn checkout https://php52-backports.googlecode.com/svn/trunk/ php52-backports</pre>

Download security and critical patches only branch:
> <pre>svn checkout https://php52-backports.googlecode.com/svn/security/ php52-backports-security</pre>


For create a patch diff-file from the original version 5.2.17 use command like this:
> <pre>svn diff -r 2 ....</pre>


### Downloads ###
  * Last 20130717 [full trunk patch](http://php52-backports.googlecode.com/files/php52-backports-20130717.patch) (all bugfixes, maybe is not stable)
  * Last 20130717 [security branch patch](http://php52-backports.googlecode.com/files/php52-backports-security-20130717.patch) (critical security bugfixes / FreeBSD port / stable / recommended)

  * [Deprecated](http://code.google.com/p/php52-backports/downloads/list?can=1) downloads (for lang/php52 port only)

### How to use ###
<pre>
cd php-5.2.17<br>
download patch<br>
patch -p1 -i php52-backports-*.patch<br>
<br>
configure && build && install as you want<br>
</pre>


### Changelog ###
See also [SVN repo changes](http://code.google.com/p/php52-backports/source/list)

_2013-07-17_
> trunk/security
  * - CVE-2013-4113 ([issue 19](https://code.google.com/p/php52-backports/issues/detail?id=19)), [issue 16](https://code.google.com/p/php52-backports/issues/detail?id=16), [issue 17](https://code.google.com/p/php52-backports/issues/detail?id=17), [issue 18](https://code.google.com/p/php52-backports/issues/detail?id=18) fixes
  * - timezonedb 2013.4 (2013d)
  * - +[PHP 5.2.17\_15](http://www.freebsd.org/cgi/query-pr.cgi?pr=181449) FreeBSD port (security patch)

_2013-03-20_
> trunk/security
  * - CVE-2013-1635, CVE-2013-1643, timezonedb 2013.2 (2013b)
  * - +[PHP 5.2.17\_14](http://www.freebsd.org/cgi/query-pr.cgi?pr=177203) FreeBSD port (security patch)

_2012-11-14_
> trunk/security
  * - Timezone database updated to version 2012.9 (2012i)
  * - +[PHP 5.2.17\_12](http://www.freebsd.org/cgi/query-pr.cgi?pr=173685) FreeBSD port

_2012-09-24_
> trunk/security:
  * - CVE-2006-7243 , CVE-2012-4388 fix

_2012-09-11_
> trunk:
  * [Issue 1](https://code.google.com/p/php52-backports/issues/detail?id=1), [Issue 13](https://code.google.com/p/php52-backports/issues/detail?id=13) fix
> trunk/security:
  * - timezonedb.h updated to version 2012.5 (2012e) (from 2011.13 (2011m))
> security:
  * - CVE-2011-1398 [r73](https://code.google.com/p/php52-backports/source/detail?r=73) (fixed in trunk as bug-60227 [r30](https://code.google.com/p/php52-backports/source/detail?r=30)) The sapi\_header\_op function in main/SAPI.c in PHP before 5.3.11 does not properly handle %0D sequences
  * - +[PHP 5.2.17\_11](http://www.freebsd.org/cgi/query-pr.cgi?pr=171583) FreeBSD port

_2012-08-26_
> trunk:
  * - CVE-2012-0789 [r67](https://code.google.com/p/php52-backports/source/detail?r=67), bug-62763 [r68](https://code.google.com/p/php52-backports/source/detail?r=68), bug-62839 [r69](https://code.google.com/p/php52-backports/source/detail?r=69), bug-62499 [r70](https://code.google.com/p/php52-backports/source/detail?r=70), bug-62715 [r71](https://code.google.com/p/php52-backports/source/detail?r=71)
> security:
  * - CVE-2012-0789 [r72](https://code.google.com/p/php52-backports/source/detail?r=72)

_2012-08-08_
> trunk/security:
  * - Linux distros compilation [issue 11](https://code.google.com/p/php52-backports/issues/detail?id=11) ([r66](https://code.google.com/p/php52-backports/source/detail?r=66) [r65](https://code.google.com/p/php52-backports/source/detail?r=65))

> security:
  * - CVE-2012-3365 open\_basedir bypass in sqlite [r61](https://code.google.com/p/php52-backports/source/detail?r=61)
  * - Improve overflow checks CVE-2012-2688 [r64](https://code.google.com/p/php52-backports/source/detail?r=64)

> trunk:
  * - bug-61546 [r54](https://code.google.com/p/php52-backports/source/detail?r=54), bug-61713 [r55](https://code.google.com/p/php52-backports/source/detail?r=55), bug-61730 [r56](https://code.google.com/p/php52-backports/source/detail?r=56), bug-61755 [r57](https://code.google.com/p/php52-backports/source/detail?r=57), bug-61764 [r58](https://code.google.com/p/php52-backports/source/detail?r=58), bug-61948 [r59](https://code.google.com/p/php52-backports/source/detail?r=59), bug-69161 [r60](https://code.google.com/p/php52-backports/source/detail?r=60)

_2012-06-23_
> trunk:
  * - bug-62432 [r51](https://code.google.com/p/php52-backports/source/detail?r=51), bug-62146 [r49](https://code.google.com/p/php52-backports/source/detail?r=49), bug-62064 [r48](https://code.google.com/p/php52-backports/source/detail?r=48), CVE-2012-3365 [r47](https://code.google.com/p/php52-backports/source/detail?r=47)
  * - Improve overflow checks CVE-2012-2688 [r52](https://code.google.com/p/php52-backports/source/detail?r=52)

_2012-06-21_
> security / trunk
  * - CVE-2012-2688 [r44](https://code.google.com/p/php52-backports/source/detail?r=44), fixes in php\_variables.c [r45](https://code.google.com/p/php52-backports/source/detail?r=45)
  * - +[PHP 5.2.17\_10](http://www.freebsd.org/cgi/query-pr.cgi?pr=170063) FreeBSD port

_2012-06-27_
> trunk:
  * - compilation issue Z\_SET\_ISREF\_PP/Z\_ADDREF\_PP in ext/soap/php\_encoding.c
  * - compilation issue zend\_alter\_ini\_entry\_ex on Linux systems fix in main/php\_variables.c (now CVE-2012-0830 patched as in Debian Linux)
  * - CVE-2012-0057
> security:
  * - compilation issue zend\_alter\_ini\_entry\_ex on Linux systems fix in main/php\_variables.c (now CVE-2012-0830 patched as in Debian Linux)
  * - CVE-2012-0057, CVE-2011-1469 (was fixed in trunk as bug-54092), CVE-2011-1470 (trunk bug-53579)

_2012-05-26_
> security / trunk
  * - CVE-2012-2311 fix (patch from v.a.popov)
  * - magic\_quotes\_gpc fix for regression introduced by CVE-2012-0831 fix
  * - CVE-2012-2336 (with fastcgi compilation issues in [r35](https://code.google.com/p/php52-backports/source/detail?r=35) [r36](https://code.google.com/p/php52-backports/source/detail?r=36))
  * - +[PHP 5.2.17\_9](http://www.freebsd.org/cgi/query-pr.cgi?pr=169272) FreeBSD port

_2012-05-04_
> trunk
  * - CVE-2012-1172, CVE-2012-1823, bugfixes 61650, 61165, 61095, 61000, 60801, 60227, 60222

> security
  * - CVE-2012-1172, CVE-2012-1823
  * - +[PHP 5.2.17\_8](http://www.freebsd.org/cgi/query-pr.cgi?pr=164849) FreeBSD port

_2012-02-16_
> security
  * - CVE-2012-0781 (bug-54682 in trunk), CVE-2011-4153, CVE-2012-0788, CVE-2012-0831

> trunk
  * - CVE-2011-4153, CVE-2012-0788, CVE-2012-0831

_2012-02-03_
> security / trunk
  * - CVE-2012-0830

_2012-02-02_
> security branch
  * - CVE-2011-1466 (fixed in trunk 2011-09-17 as [bug-53574](https://bugs.php.net/bug.php?id=53574)), CVE-2011-1471 (fixed in trunk 2011-09-17 as [bug-49072](https://bugs.php.net/bug.php?id=49072))

_2012-01-17_
> trunk
  * - CVE-2011-4566, bugfixes 60206, 60138, 60120, 55674, 55509, 55504, 52461, 55366, 55273, 52624, 43200, 54682, 60455, 60183, 55478 from centos.alt.ru

> security
  * - CVE-2011-4566 fix (Integer overflow during the parsing of invalid exif header)
  * - +[PHP 5.2.17\_6](http://www.freebsd.org/cgi/query-pr.cgi?pr=ports/164286) FreeBSD port

_2012-01-03_
> security / trunk
  * - Added php-5.2-max-input-vars patch max\_input\_vars directive to prevent attacks based on hash collisions - CVE-2011-4885
  * - +[PHP 5.2.17\_5](http://www.freebsd.org/cgi/query-pr.cgi?pr=163782) FreeBSD port (security  branch)

_2011-10-30_
> security / trunk
  * - New timezonedb.h (abolition of winter time)
  * - +[PHP 5.2.17\_4](http://www.freebsd.org/cgi/query-pr.cgi?pr=162165) FreeBSD port (from security  branch)

_2011-09-17_
> trunk
  * - CVE-2011-2202, CVE-2011-1938, CVE-2011-1148, CVE-2011-0708, CVE-2011-1092, CVE-2011-0421
  * - Fixes from https://bugs.php.net/ - bug-54055, bug-53577, bug-48484, bug-48607, bug-53574, bug-52290, bug-52063, bug-53924, bug-53150, bug-52209, bug-47435, bug-53377, bug-39847, bug-53630, bug-51336, bug-53515, bug-54092, bug-53903, bug-54089, bug-53603, bug-53854, bug-53579, bug-53568, bug-49072, bug-55399, bug-55082, bug-55014, bug-54180, bug-54137, bug-53848, bug-52935, bug-51997, bug-50363, bug-48465, bug-54529, bug-52496, bug-54242, bug-54121, bug-53037, bug-54269, bug-54601, bug-54440, bug-54494, bug-54221, bug-52104, bug-54329, bug-53782, bug-54318, bug-55323, bug-54312, bug-51958, bug-54946

> Thanks to CentOS.alt.ru for great work http://centos.alt.ru/?p=571

_2011-09-17_
> security
  * - CVE-2011-2202, CVE-2011-1938, CVE-2011-1148, CVE-2011-0708, CVE-2011-1092, CVE-2011-0421
  * - +[PHP 5.2.17\_3](http://www.freebsd.org/cgi/query-pr.cgi?pr=ports/160805) FreeBSD port (from security  branch, splited patchfiles only)

_2011-09-17_
  * Project started