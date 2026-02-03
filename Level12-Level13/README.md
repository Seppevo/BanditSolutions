# Level 12 → Level 13

## 🎯 Goal
The password for the next level is stored in the file data.txt, which is a hexdump of a file that has been repeatedly compressed. For this level it may be useful to create a directory under /tmp in which you can work. Use mkdir with a hard to guess directory name. Or better, use the command “mktemp -d”. Then copy the datafile using cp, and rename it using mv (read the manpages!)

## 🏁 Last Flag
 **7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4**

## 💡 Solution

```bash
bandit12@bandit:~$ mktemp -d
/tmp/tmp.dYBgv09wsD
bandit12@bandit:/tmp/tmp.dYBgv09wsD$ mv data.txt hexdumpdata
bandit12@bandit:/tmp/tmp.dYBgv09wsD$ xxd -r hexdumpdata compressedata
bandit12@bandit:/tmp/tmp.dYBgv09wsD$ ls
compressedata  hexdumpdata
bandit12@bandit:/tmp/tmp.dYBgv09wsD$ cat compressedata 
␦h�@щ��AFM�@ё�h␦��h��2�i���&���␦���#C�40�h����hh�hhh�L�M���0�� 2h��h4b4�hi�␦z�@�����4
                                                                  �d��h`5A,���{�G��i0�P��d�@1/KȰ
                                                                                                �l�ת3j폻{�?�DX�N����a.�'������-hf��'Tu�9
                        ��x(F����C��9z��#*ڛ�M�]J��2䔮�'�0�S<f�`��Fp�2+qt��R��
&{qe �w��"�35OƎ����Z
�hȔ'�7<bandit12@bandit:/tmp/tmp.dYBgv09wsD$ ls
compressedata  hexdumpdata
bandit12@bandit:/tmp/tmp.dYBgv09wsD$ cat hexdumpdata 
00000000: 1f8b 0808 2817 ee68 0203 6461 7461 322e  ....(..h..data2.
00000010: 6269 6e00 013c 02c3 fd42 5a68 3931 4159  bin..<...BZh91AY
00000020: 2653 59cc 46b5 2d00 0018 ffff da5f e6e3  &SY.F.-......_..
00000030: 9fcd f59d bc69 ddd7 f7ff a7e7 dbdd b59f  .....i..........
00000040: fff7 cfdd ffbf bbdf ffff ff5e b001 3b58  ...........^..;X
00000050: 2406 8000 00d0 6834 6234 d000 6869 9000  $.....h4b4..hi..
00000060: 1a7a 8003 40d0 01a1 a006 8188 340d 1a68  .z..@.......4..h
00000070: d340 d189 e906 8f41 0346 4d94 40d1 91a0  .@.....A.FM.@...
00000080: 681a 0681 a068 0680 c400 3207 a269 a189  h....h....2..i..
00000090: a326 8000 c800 c81a 1883 1000 00d0 c023  .&.............#
000000a0: 4311 a034 30ca 6800 0680 0681 a680 6868  C..40.h.......hh
000000b0: d068 6868 c04c d400 0003 4d06 87a8 d000  .hhh.L....M.....
000000c0: 3086 8c20 3268 068d 000c 9a64 0698 8d04  0.. 2h.....d....
000000d0: 0600 6860 3541 2c85 c8e1 7bc9 479e e369  ..h`5A,...{.G..i
000000e0: 30a1 0250 82e9 64ef 9d40 312f 4bc8 b00f  0..P..d..@1/K...
000000f0: 0c8f 026c d5ca 1008 d7aa 336a ed8f bb7b  ...l......3j...{
00000100: b43f d544 1658 824e a4af 9ce5 612e 8a27  .?.D.X.N....a..'
00000110: c303 0512 cbff dccd f42d 6866 ceec 8127  .........-hf...'
00000120: 5475 ed39 100b f897 7828 46e2 fdf3 efa7  Tu.9....x(F.....
00000130: 43b0 1701 a114 397a 1d81 8d1f 1f23 2ada  C.....9z.....#*.
00000140: 9b18 ee4d d05d 4ae3 d032 e494 ae98 27b0  ...M.]J..2....'.
00000150: 30a0 533c 6696 60ad c546 70c4 322b 7174  0.S<f.`..Fp.2+qt
00000160: 8bb1 52c6 ed0a 267b 7165 208b 77fe 1294  ..R...&{qe .w...
00000170: 2280 3311 354f c68e e004 93e3 abf4 5a0a  ".3.5O........Z.
00000180: a568 c894 27c2 9015 49bb 0147 c253 8e73  .h..'...I..G.S.s
00000190: 2fdd 90e1 6871 c692 1d67 5ebc a5f9 b8a1  /...hq...g^.....
000001a0: 3913 f073 1919 b628 9ae2 c1bf 15ee 493a  9..s...(......I:
000001b0: e375 4d23 71e0 4934 c7a2 15ff 985c a0ba  .uM#q.I4.....\..
000001c0: 9e65 d613 313d 7cef 512a 32bf 835e 50d6  .e..1=|.Q*2..^P.
000001d0: a54f 57ba bceb 6944 03c8 8a50 3542 9140  .OW...iD...P5B.@
000001e0: eb51 0f4c 8a23 9401 0246 0457 d1c0 c33e  .Q.L.#...F.W...>
000001f0: c328 2de7 3d1d 64be 4190 36b0 b803 4f80  .(-.=.d.A.6...O.
00000200: 40bc 3960 ac5e 13a9 3a77 0162 d662 7659  @.9`.^..:w.b.bvY
00000210: fdfd 9535 1188 8588 e8e5 a78d 9b24 c066  ...5.........$.f
00000220: 91c6 4212 fac6 4ed8 ce48 161f cc44 215f  ..B...N..H...D!_
00000230: 330c 5ed7 2709 e578 6efd 3775 c703 8aa1  3.^.'..xn.7u....
00000240: 10b6 2c5d 16bf f352 c7ff c5dc 914e 1424  ..,]...R.....N.$
00000250: 3311 ad4b 40d0 18b2 373c 0200 00         3..K@...7<...
bandit12@bandit:/tmp/tmp.dYBgv09wsD$ mv compressedata compressed.gz
bandit12@bandit:/tmp/tmp.dYBgv09wsD$ ls
compressed.gz  hexdumpdata
bandit12@bandit:/tmp/tmp.dYBgv09wsD$ gzip -d compressed.gz 
bandit12@bandit:/tmp/tmp.dYBgv09wsD$ ls
compressed  hexdumpdata
bandit12@bandit:/tmp/tmp.dYBgv09wsD$ cat compressed 
␦h�@щ��AFM�@ё�h␦��h��2�i���&���␦���#C�40�h����hh�hhh�L�M���0�� 2h����4
                                                                  �d��h`5A,���{�G��i0�P��d�@1/KȰ
                                                                                                �l�ת3j폻{�?�DX�N����a.�'������-hf��'Tu�9
                        ��x(F����C��9z��#*ڛ�M�]J��2䔮�'�0�S<f�`��Fp�2+qt��R��
&{qe �w��"�35OƎ����Z
�hȔ'bandit12@bandit:/tmp/tmp.dYBgv09wsD$ xxd compressed 
00000000: 425a 6839 3141 5926 5359 cc46 b52d 0000  BZh91AY&SY.F.-..
00000010: 18ff ffda 5fe6 e39f cdf5 9dbc 69dd d7f7  ...._.......i...
00000020: ffa7 e7db ddb5 9fff f7cf ddff bfbb dfff  ................
00000030: ffff 5eb0 013b 5824 0680 0000 d068 3462  ..^..;X$.....h4b
00000040: 34d0 0068 6990 001a 7a80 0340 d001 a1a0  4..hi...z..@....
00000050: 0681 8834 0d1a 68d3 40d1 89e9 068f 4103  ...4..h.@.....A.
00000060: 464d 9440 d191 a068 1a06 81a0 6806 80c4  FM.@...h....h...
00000070: 0032 07a2 69a1 89a3 2680 00c8 00c8 1a18  .2..i...&.......
00000080: 8310 0000 d0c0 2343 11a0 3430 ca68 0006  ......#C..40.h..
00000090: 8006 81a6 8068 68d0 6868 68c0 4cd4 0000  .....hh.hhh.L...
000000a0: 034d 0687 a8d0 0030 868c 2032 6806 8d00  .M.....0.. 2h...
000000b0: 0c9a 6406 988d 0406 0068 6035 412c 85c8  ..d......h`5A,..
000000c0: e17b c947 9ee3 6930 a102 5082 e964 ef9d  .{.G..i0..P..d..
000000d0: 4031 2f4b c8b0 0f0c 8f02 6cd5 ca10 08d7  @1/K......l.....
000000e0: aa33 6aed 8fbb 7bb4 3fd5 4416 5882 4ea4  .3j...{.?.D.X.N.
000000f0: af9c e561 2e8a 27c3 0305 12cb ffdc cdf4  ...a..'.........
00000100: 2d68 66ce ec81 2754 75ed 3910 0bf8 9778  -hf...'Tu.9....x
00000110: 2846 e2fd f3ef a743 b017 01a1 1439 7a1d  (F.....C.....9z.
00000120: 818d 1f1f 232a da9b 18ee 4dd0 5d4a e3d0  ....#*....M.]J..
00000130: 32e4 94ae 9827 b030 a053 3c66 9660 adc5  2....'.0.S<f.`..
00000140: 4670 c432 2b71 748b b152 c6ed 0a26 7b71  Fp.2+qt..R...&{q
00000150: 6520 8b77 fe12 9422 8033 1135 4fc6 8ee0  e .w...".3.5O...
00000160: 0493 e3ab f45a 0aa5 68c8 9427 c290 1549  .....Z..h..'...I
00000170: bb01 47c2 538e 732f dd90 e168 71c6 921d  ..G.S.s/...hq...
00000180: 675e bca5 f9b8 a139 13f0 7319 19b6 289a  g^.....9..s...(.
00000190: e2c1 bf15 ee49 3ae3 754d 2371 e049 34c7  .....I:.uM#q.I4.
000001a0: a215 ff98 5ca0 ba9e 65d6 1331 3d7c ef51  ....\...e..1=|.Q
000001b0: 2a32 bf83 5e50 d6a5 4f57 babc eb69 4403  *2..^P..OW...iD.
000001c0: c88a 5035 4291 40eb 510f 4c8a 2394 0102  ..P5B.@.Q.L.#...
000001d0: 4604 57d1 c0c3 3ec3 282d e73d 1d64 be41  F.W...>.(-.=.d.A
000001e0: 9036 b0b8 034f 8040 bc39 60ac 5e13 a93a  .6...O.@.9`.^..:
000001f0: 7701 62d6 6276 59fd fd95 3511 8885 88e8  w.b.bvY...5.....
00000200: e5a7 8d9b 24c0 6691 c642 12fa c64e d8ce  ....$.f..B...N..
00000210: 4816 1fcc 4421 5f33 0c5e d727 09e5 786e  H...D!_3.^.'..xn
00000220: fd37 75c7 038a a110 b62c 5d16 bff3 52c7  .7u......,]...R.
00000230: ffc5 dc91 4e14 2433 11ad 4b40            ....N.$3..K@
bandit12@bandit:/tmp/tmp.dYBgv09wsD$ ls
compressed  hexdumpdata
bandit12@bandit:/tmp/tmp.dYBgv09wsD$ mv compressed compressed.bz2
bandit12@bandit:/tmp/tmp.dYBgv09wsD$ ls
compressed.bz2  hexdumpdata
bandit12@bandit:/tmp/tmp.dYBgv09wsD$ bzip2 -d compressed.bz2 
bandit12@bandit:/tmp/tmp.dYBgv09wsD$ ls
compressed  hexdumpdata
bandit12@bandit:/tmp/tmp.dYBgv09wsD$ cat compressed 
(�hdata4.bin��OH�q��St��IDP~h�T�ߟ�&⿩�
A�`�K����u0P�`(�H��(<H�x�`D�у7/yTPj͎
v�?�~]>���>f�
���k�.u������q�R�g��V�
<fB�"B���e���Rf�ϵ����a\��C�W��#X�յ��O�bw���|����Pl_y\������k,���+b.�Wm�u��;Z�o̜��Ŗ�Ꮿ���:���}N�t$1�7X���N�%e�DZ�gm�d:�d�jq��������/���n��.�~ؖ
                          ��_�2�V������`���˒������������6~��O�;�ʚ���d�o^�4+&��q�'�뭝�������^l2,���ض:�Pbandit12@bandit:/tmp/tmp.dYBgv09wsD$ mv compressed compressed.gz
bandit12@bandit:/tmp/tmp.dYBgv09wsD$ gzip -d compressed.gz 
bandit12@bandit:/tmp/tmp.dYBgv09wsD$ ls
compressed  hexdumpdata
bandit12@bandit:/tmp/tmp.dYBgv09wsD$ cat compressed 
data5.bin0000644000000000000000000002400015073413450011242 0ustar  rootrootdata6.bin0000644000000000000000000000I22L�SL�d␦<��Pi~��2hɓ 0u��␦��r�y?�rootBZh91AY&SY�I����j��}�� [#�ta�@f �
�P��TŴ��4H�*C�'jb�7)�z4���t��p�&5��Z�4�V#´e^�y
ڼ�+>�K-��J�՞lBI��L*�
                    6;>�d.(J"N��d9�d��(�2@@?��"�(HD$���
bandit12@bandit:/tmp/tmp.dYBgv09wsD$ mv compressed compressed.tar
bandit12@bandit:/tmp/tmp.dYBgv09wsD$ tar -xf compressed.tar 
bandit12@bandit:/tmp/tmp.dYBgv09wsD$ ls
compressed.tar  data5.bin  hexdumpdata
bandit12@bandit:/tmp/tmp.dYBgv09wsD$ tar -xf data5.bin
bandit12@bandit:/tmp/tmp.dYBgv09wsD$ ls
compressed.tar  data5.bin  data6.bin  hexdumpdata
bandit12@bandit:/tmp/tmp.dYBgv09wsD$ xxd data6.bin 
00000000: 425a 6839 3141 5926 5359 8849 ff13 0000  BZh91AY&SY.I....
00000010: 8d7f cfdc 6a00 c0c0 7dff e120 5b23 8074  ....j...}.. [#.t
00000020: 61fe 8000 0840 0000 6682 0108 014c 0820  a....@..f....L. 
00000030: 0094 0d49 3d08 3232 0003 4c80 0f53 4c9a  ...I=.22..L..SL.
00000040: 641a 3ca7 a350 6914 7ea9 9032 6800 c993  d.<..Pi.~..2h...
00000050: 09a1 a01a 068c 8d03 72dd 793f c810 180c  ........r.y?....
00000060: 0204 0d07 8d50 9691 54c5 b411 101e f798  .....P..T.......
00000070: 3448 bc2a 4385 276a 62d5 3729 b77a 34fb  4H.*C.'jb.7).z4.
00000080: 0fcc dc1d 74c3 0004 ed70 02aa 2635 c0fd  ....t....p..&5..
00000090: 5a81 34c0 5623 c2b4 655e dd79 0ada bc86  Z.4.V#..e^.y....
000000a0: 2b3e d24b 2d8e ee4a f6d5 9e6c 4249 c5d1  +>.K-..J...lBI..
000000b0: 4c2a fa0e 0c10 0f36 3b3e e864 2e28 4a02  L*.....6;>.d.(J.
000000c0: 224e a3c8 6439 8964 aa85 28b0 3240 403f  "N..d9.d..(.2@@?
000000d0: 8bb9 229c 2848 4424 ff89 80              ..".(HD$...
bandit12@bandit:/tmp/tmp.dYBgv09wsD$ ls
compressed.tar  data5.bin  data6.bin.out  hexdumpdata
bandit12@bandit:/tmp/tmp.dYBgv09wsD$ tar -xf data6.bin.out
bandit12@bandit:/tmp/tmp.dYBgv09wsD$ ls
compressed.tar  data5.bin  data6.bin.out  data8.bin  hexdumpdata
bandit12@bandit:/tmp/tmp.dYBgv09wsD$ xxd data8.bin 
00000000: 1f8b 0808 2817 ee68 0203 6461 7461 392e  ....(..h..data9.
00000010: 6269 6e00 0bc9 4855 2848 2c2e 2ecf 2f4a  bin...HU(H,.../J
00000020: 51c8 2c56 70f3 374d 2977 2b4e 3648 4e4a  Q.,Vp.7M)w+N6HNJ
00000030: f4cc f430 c8b0 f032 4a0d cd2e 362a 4b09  ...0...2J...6*K.
00000040: 7129 77cc e302 003e de32 4131 0000 00    q)w....>.2A1...
bandit12@bandit:/tmp/tmp.dYBgv09wsD$ mv data8.bin data8.gz
bandit12@bandit:/tmp/tmp.dYBgv09wsD$ gzip -d data8.gz 
bandit12@bandit:/tmp/tmp.dYBgv09wsD$ ls
compressed.tar  data5.bin  data6.bin.out  data8  hexdumpdata
bandit12@bandit:/tmp/tmp.dYBgv09wsD$ cat data8
The password is FO5dwFsc0cbaIiH0h8J2eUks2vdTDwAn

```
