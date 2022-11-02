### split a file

```bash
$ lc
-rw-rw-r-- 1 rog rog 195M Nov  1 21:51 en.stm32cubeprg-lin_v2-11-0.zip
```

split it to many files of 10M size:

```bash
$ split -b 10M en.stm32cubeprg-lin_v2-11-0.zip stm32-cube-programer.tar.
```

Then we will see a lot of files:
```bash
$ lc
total 390M
-rw-rw-r-- 1 rog rog 195M Nov  1 21:51 en.stm32cubeprg-lin_v2-11-0.zip
-rw-rw-r-- 1 rog rog    0 Nov  1 22:50 README.md
-rw-rw-r-- 1 rog rog  10M Nov  1 22:49 stm32-cube-programer.tar.aa
-rw-rw-r-- 1 rog rog  10M Nov  1 22:49 stm32-cube-programer.tar.ab
-rw-rw-r-- 1 rog rog  10M Nov  1 22:49 stm32-cube-programer.tar.ac
-rw-rw-r-- 1 rog rog  10M Nov  1 22:49 stm32-cube-programer.tar.ad
-rw-rw-r-- 1 rog rog  10M Nov  1 22:49 stm32-cube-programer.tar.ae
-rw-rw-r-- 1 rog rog  10M Nov  1 22:49 stm32-cube-programer.tar.af
-rw-rw-r-- 1 rog rog  10M Nov  1 22:49 stm32-cube-programer.tar.ag
-rw-rw-r-- 1 rog rog  10M Nov  1 22:49 stm32-cube-programer.tar.ah
-rw-rw-r-- 1 rog rog  10M Nov  1 22:49 stm32-cube-programer.tar.ai
-rw-rw-r-- 1 rog rog  10M Nov  1 22:49 stm32-cube-programer.tar.aj
-rw-rw-r-- 1 rog rog  10M Nov  1 22:49 stm32-cube-programer.tar.ak
-rw-rw-r-- 1 rog rog  10M Nov  1 22:49 stm32-cube-programer.tar.al
-rw-rw-r-- 1 rog rog  10M Nov  1 22:49 stm32-cube-programer.tar.am
-rw-rw-r-- 1 rog rog  10M Nov  1 22:49 stm32-cube-programer.tar.an
-rw-rw-r-- 1 rog rog  10M Nov  1 22:49 stm32-cube-programer.tar.ao
-rw-rw-r-- 1 rog rog  10M Nov  1 22:49 stm32-cube-programer.tar.ap
-rw-rw-r-- 1 rog rog  10M Nov  1 22:49 stm32-cube-programer.tar.aq
-rw-rw-r-- 1 rog rog  10M Nov  1 22:49 stm32-cube-programer.tar.ar
-rw-rw-r-- 1 rog rog  10M Nov  1 22:49 stm32-cube-programer.tar.as
-rw-rw-r-- 1 rog rog 4.9M Nov  1 22:49 stm32-cube-programer.tar.at
```

To merge those files:
```bash
$ cat stm32-cube-programer.tar.* > en.stm32cubeprg-lin_v2-11-0.zip
```

