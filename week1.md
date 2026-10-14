
niixyy01
uid=1000(niixyy01) gid=1000(niixyy01) groups=1000(niixyy01),4(adm),24(cdrom),27(sudo),30(dip),46(plugdev),100(users)

USER         PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND
root           1  0.0  0.1  24276 15452 ?        Ss   08:56   0:01 /sbin/init
root           2  0.0  0.0   3804  2512 hvc0     Sl+  08:56   0:00 /init
root           3  0.0  0.0   3664  2132 hvc0     S+   08:56   0:00 init-watcher
root           8  0.0  0.0   3804  2276 hvc0     Sl+  08:56   0:00 plan9 --control-socket 7 --log-level 4 --server-fd 8 --pipe-fd 10 --log-truncate
root          48  0.0  0.2  50664 19332 ?        S<s  08:56   0:00 /usr/lib/systemd/systemd-journald
systemd+      79  0.0  0.1  22416 14588 ?        Ss   08:56   0:00 /usr/lib/systemd/systemd-resolved
root          88  0.0  0.1  34776 12112 ?        Ss   08:56   0:01 /usr/lib/systemd/systemd-udevd
root         110  0.0  0.0   2888  2012 ?        Ss   08:56   0:00 /bin/sh /usr/lib/systemd/scripts/chronyd-starter.sh -n -F 1
root         111  0.0  0.0   4472  3188 ?        Ss   08:56   0:00 /usr/sbin/cron -f -P
message+     112  0.0  0.0   8824  5560 ?        Ss   08:56   0:00 @dbus-daemon --system --address=systemd: --nofork --nopidfile --systemd-activation --syslog-only
root         116  0.0  0.3  44096 29800 ?        Ss   08:56   0:00 /usr/bin/python3 /usr/bin/networkd-dispatcher --run-startup-triggers
root         152  0.0  0.1  18568  9548 ?        Ss   08:56   0:00 /usr/lib/systemd/systemd-logind
syslog       178  0.0  0.0 220548  5996 ?        Ssl  08:56   0:00 /usr/sbin/rsyslogd -n -iNONE
root         199  0.0  0.0   5492  2816 tty1     Ss+  08:56   0:00 /usr/sbin/agetty --noreset --noclear --issue-file=/etc/issue:/etc/issue.d:/run/issue.d:/usr/lib/issue.d - linux


State   Recv-Q   Send-Q      Local Address:Port       Peer Address:Port  Process
LISTEN  0        4096        127.0.0.53%lo:domain          0.0.0.0:*
         skmem:(r0,rb131072,t0,tb16384,f0,w0,o0,bl0,d0)
LISTEN  0        4096           127.0.0.54:domain          0.0.0.0:*
         skmem:(r0,rb131072,t0,tb16384,f0,w0,o0,bl0,d0)
LISTEN  0        1000       10.255.255.254:domain          0.0.0.0:*
         skmem:(r0,rb131072,t0,tb16384,f0,w0,o0,bl0,d0)

State   Recv-Q   Send-Q      Local Address:Port       Peer Address:Port  Process
LISTEN  0        4096        127.0.0.53%lo:domain          0.0.0.0:*
         skmem:(r0,rb131072,t0,tb16384,f0,w0,o0,bl0,d0)
LISTEN  0        4096           127.0.0.54:domain          0.0.0.0:*
         skmem:(r0,rb131072,t0,tb16384,f0,w0,o0,bl0,d0)
LISTEN  0        1000       10.255.255.254:domain          0.0.0.0:*
         skmem:(r0,rb131072,t0,tb16384,f0,w0,o0,bl0,d0)

               total        used        free      shared  buff/cache   available
Mem:           7.5Gi       502Mi       6.8Gi       4.1Mi       318Mi       7.0Gi
Swap:          2.0Gi          0B       2.0Gi
8

