```bash
dell@DELL3521 /d/docker1.7.1
$ docker run -it ubuntu bash
root@4b58852782f4:/# lsb_release -a
No LSB modules are available.
Distributor ID: Ubuntu
Description:    Ubuntu 14.04.2 LTS
Release:        14.04
Codename:       trusty
root@4b58852782f4:/# ls
bin   dev  home  lib64  mnt  proc  run   srv  tmp  var
boot  etc  lib   media  opt  root  sbin  sys  usr
root@4b58852782f4:/# pwd
/
root@4b58852782f4:/# ls usr
bin  games  include  lib  local  sbin  share  src
root@4b58852782f4:/# ls sys
block  class  devices   fs          kernel  power
bus    dev    firmware  hypervisor  module
root@4b58852782f4:/# ls sys/kernel
boot_params  iommu_groups        mm             security
debug        kexec_crash_loaded  notes          uevent_helper
fscache      kexec_crash_size    profiling      uevent_seqnum
fscaps       kexec_loaded        rcu_expedited  vmcoreinfo
root@4b58852782f4:/# ls bin
bash           egrep      mountpoint               ss
bunzip2        false      mt                       stty
bzcat          fgconsole  mt-gnu                   su
bzcmp          fgrep      mv                       sync
bzdiff         findmnt    nc                       tailf
bzegrep        grep       nc.openbsd               tar
bzexe          gunzip     netcat                   tempfile
bzfgrep        gzexe      netstat                  touch
bzgrep         gzip       nisdomainname            true
bzip2          hostname   open                     udevadm
bzip2recover   ip         openvt                   umount
bzless         kbd_mode   pidof                    uname
bzmore         kill       ping                     uncompress
cat            kmod       ping6                    unicode_start
chgrp          less       plymouth                 vdir
chmod          lessecho   plymouth-upstart-bridge  which
chown          lessfile   ps                       whiptail
chvt           lesskey    pwd                      ypdomainname
cp             lesspipe   rbash                    zcat
cpio           ln         readlink                 zcmp
dash           loadkeys   rm                       zdiff
date           login      rmdir                    zegrep
dd             ls         run-parts                zfgrep
df             lsblk      running-in-container     zforce
dir            lsmod      sed                      zgrep
dmesg          mkdir      setfont                  zless
dnsdomainname  mknod      setupcon                 zmore
domainname     mktemp     sh                       znew
dumpkeys       more       sh.distrib
echo           mount      sleep
root@4b58852782f4:/# ls sys/hypervisor
root@4b58852782f4:/# ls tmp
root@4b58852782f4:/# ls dev
console  full  kcore   null  pts     shm     stdin   tty      zero
fd       fuse  mqueue  ptmx  random  stderr  stdout  urandom
root@4b58852782f4:/# ls lib64
ld-linux-x86-64.so.2
root@4b58852782f4:/# ls srv
root@4b58852782f4:/# ls var
backups  cache  lib  local  lock  log  mail  opt  run  spool  tmp
root@4b58852782f4:/# ls usr/bin
2to3-3.4                 install            pygettext3
[                        instmodsh          pygettext3.4
a2p                      ionice             python3
addpart                  ipcmk              python3.4
apt                      ipcrm              python3.4m
apt-cache                ipcs               python3m
apt-cdrom                ischroot           pyvenv-3.4
apt-config               join               rename
apt-extracttemplates     json_pp            rename.ul
apt-ftparchive           kbdinfo            renice
apt-get                  last               reset
apt-key                  lastb              resizecons
apt-mark                 lastlog            resizepart
apt-sortpkgs             lcf                rev
arch                     ldd                rgrep
awk                      less               routef
base64                   lessecho           routel
basename                 lessfile           rtstat
bashbug                  lesskey            run-mailcap
c2ph                     lesspipe           runcon
captoinfo                libnetcfg          rview
catchsegv                line               s2p
cautious-launcher        link               savelog
chage                    linux32            screendump
chattr                   linux64            script
chcon                    lnstat             scriptreplay
chfn                     loadkeys           sdiff
chkdupexe                loadunimap         see
chrt                     locale             select-editor
chsh                     localedef          sensible-browser
ckbcomp                  lockfile-check     sensible-editor
cksum                    lockfile-create    sensible-pager
clear                    lockfile-remove    seq
clear_console            lockfile-touch     service
cmp                      logger             setarch
codepage                 logname            setkeycodes
comm                     lsattr             setleds
compose                  lsb_release        setlogcons
config_data              lscpu              setmetamode
corelist                 lsinitramfs        setsid
cpan                     lspgpot            setterm
cpan2dist                mail-lock          sg
cpanp                    mail-touchlock     sha1sum
cpanp-run-perl           mail-unlock        sha224sum
crontab                  mapscrn            sha256sum
csplit                   mawk               sha384sum
ctstat                   mcookie            sha512sum
cut                      md5sum             shasum
ddate                    md5sum.textutils   showconsolefont
deallocvt                mesg               showkey
deb-systemd-helper       mk_modmap          shred
deb-systemd-invoke       mkfifo             shuf
debconf                  namei              skill
debconf-apt-progress     nawk               slabtop
debconf-communicate      ncurses5-config    snice
debconf-copydb           ncursesw5-config   sort
debconf-escape           newgrp             splain
debconf-set-selections   nice               split
debconf-show             nl                 splitfont
delpart                  nohup              stat
dh_pypy                  nproc              stdbuf
dh_python3               nstat              sudo
diff                     numfmt             sudoedit
diff3                    od                 sudoreplay
dircolors                oldfind            sum
dirname                  omshell            tabs
dotlockfile              pager              tac
dpkg                     partx              tail
dpkg-deb                 passwd             taskset
dpkg-divert              paste              tee
dpkg-maintscript-helper  pathchk            test
dpkg-query               pdb3               tic
dpkg-split               pdb3.4             timeout
dpkg-statoverride        perl               tload
dpkg-trigger             perl5.18.2         toe
du                       perlbug            top
dumpkeys                 perldoc            touch
edit                     perlivp            tput
editor                   perlthanks         tr
eject                    pg                 truncate
enc2xs                   pgrep              tset
env                      piconv             tsort
ex                       pinky              tty
expand                   pkill              tzselect
expiry                   pl2pm              ucf
expr                     pldd               ucfq
factor                   pmap               ucfr
faillog                  pod2html           unexpand
fallocate                pod2latex          unicode_stop
file                     pod2latex.bundled  uniq
find                     pod2man            unlink
find2perl                pod2text           unshare
flock                    pod2usage          update-alternatives
fmt                      podchecker         uptime
fold                     podselect          users
free                     pr                 vi
getconf                  prename            view
getent                   print              vim.tiny
getkeycodes              printenv           vmstat
getopt                   printf             volname
gpasswd                  prove              w
gpg                      psed               w.procps
gpg-zip                  psfaddtable        wall
gpgsplit                 psfgettable        watch
gpgv                     psfstriptable      wc
groups                   psfxtable          whereis
h2ph                     pstruct            which
h2xs                     ptar               who
head                     ptardiff           whoami
helpztags                ptargrep           x86_64
hostid                   ptx                xargs
i386                     pwdx               xsubpp
iconv                    py3clean           xxd
id                       py3compile         yes
infocmp                  py3versions        zdump
infotocap                pybuild            zipdetails
init-checkconf           pydoc3
initctl2dot              pydoc3.4

root@4b58852782f4:/# ls opt
root@4b58852782f4:/# ls run
lock  motd.dynamic  network  resolvconf  sendsigs.omit.d  shm  utmp
root@4b58852782f4:/# ls media
root@4b58852782f4:/# ls proc
1          crypto       iomem       loadavg       scsi           timer_list
31         devices      ioports     locks         self           timer_stats
acpi       diskstats    irq         meminfo       slabinfo       tty
buddyinfo  dma          kallsyms    misc          softirqs       uptime
bus        driver       kcore       modules       stat           version
cgroups    execdomains  key-users   mounts        swaps          vmallocinfo
cmdline    fb           keys        mtrr          sys            vmstat
config.gz  filesystems  kmsg        net           sysrq-trigger  zoneinfo
consoles   fs           kpagecount  pagetypeinfo  sysvipc
cpuinfo    interrupts   kpageflags  partitions    thread-self
root@4b58852782f4:/# ls proc/crypto
proc/crypto
root@4b58852782f4:/# ls proc/diskstats
proc/diskstats
root@4b58852782f4:/# ls proc/tty
driver  drivers  ldisc  ldiscs
root@4b58852782f4:/# ls boot
root@4b58852782f4:/# exit
exit
```
