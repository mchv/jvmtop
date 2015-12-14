jvmtop :lemon:
=======================

jvmtop (:lemon: flavor) is a lightweight console application to monitor all accessible, running jvms on a machine.<br>
In a top-like manner, it displays [JVM internal metrics](https://github.com/mchv/jvmtop/blob/master/doc/ExampleOutput.md) (e.g. memory information) of running java processes.

```
 jvmtop (lemon flavor) 0.1.0   amd64  8 cpus, Linux 2.6.32-27, load avg 0.12

  PID MAIN-CLASS      HPCUR HPMAX NHCUR NHMAX    CPU     GC    VM USERNAME   #T DL
 3370 rapperSimpleApp  165m  455m  109m  176m  0.12%  0.00% S6U37 web        21
11272 ver.resin.Resin [ERROR: Could not attach to VM]
27338 WatchdogManager   11m   28m   23m  130m  0.00%  0.00% S6U37 web        31
19187 m.jvmtop.JvmTop   20m 3544m   13m  130m  0.93%  0.47% S6U37 web        20
16733 artup.Bootstrap  159m  455m  166m  304m  0.12%  0.00% S6U37 web        46
```

It does also include a [CPU Console Profiler](https://github.com/patric-r/jvmtop/blob/master/doc/ConsoleProfiler.md)

```
 jvmtop (lemon flavor) 0.1.0 - 16:11:35,  amd64,  4 cpus, Linux 3.13.0-52, load avg 1.10

 Profiling PID 1397:        com.gu.contentapi.concierge.Start 

  13.03% (     5.99s) spray.httpx.encoding.DeflateCompressor.drain()
  10.35% (     4.76s) ....elasticsearch.common.netty.channel.socket.nio.Select()
   8.44% (     3.88s) scala.collection.AbstractTraversable.<init>()
   7.96% (     3.66s) ....gu.contentapi.concierge.util.JsonHelpers$$anonfun$re()
```

jvmtop (:lemon: flavor) is a convenient fork of [jvmtop](https://github.com/patric-r/jvmtop) with additional fixes.  

If you experience a problem [please fill an issue](https://github.com/mchv/jvmtop/issues)


requirements
-------------

 * JDK (JRE is not sufficient)

jvmtop has been tested with different releases of Oracle JDK, IBM JDK and OpenJDK on Linux, Solaris, FreeBSD and Windows hosts.


documentation
--------------

[Documentation](./doc/Documentation.md)

Installation
-------------

* Download the most recent tar.gz archive in [releases tab](https://github.com/mchv/jvmtop/releases)
* Extract it
* Run `./jvmtop.sh`
