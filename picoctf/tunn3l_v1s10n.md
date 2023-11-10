# tunn3l_v1s10n
**Category:** Forensics, 40 points

## Description

> Recover the flag from the attached file.

## Solution

The file initially appears as data:

┌──(user@kali)-[/media/sf_CTFs/pico/tunn3l_v1s10n]
└─$ file tunn3l_v1s10n
tunn3l_v1s10n: data

Upon examining the file, it seems to be a BMP image with an incorrect header size. Correcting the header and adjusting the image dimensions reveals the flag:

┌──(user@kali)-[/media/sf_CTFs/pico/tunn3l_v1s10n]
└─$ xxd -g 1 tunn3l_v1s10n.bmp | head -2
00000000: 42 4d 8e 26 2c 00 00 00 00 00 36 00 00 00 28 00 BM.&,.....6...(.
00000010: 00 00 6e 04 00 00 52 03 00 00 01 00 18 00 00 00 ..n...R.........


Opening the image reveals the flag: `picoCTF{qu1t3_a_v13w_2020}`.
