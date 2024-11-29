
comando: 

### Raspberry pi 4
`sudo hdparm -tT /dev/mmcblk0`

Resultado:
`/dev/mmcblk0:`
` Timing cached reads:   1858 MB in  2.00 seconds = 929.98 MB/sec`
` Timing buffered disk reads: 104 MB in  3.03 seconds =  34.32 MB/sec`

### Raspberry pi 5
sudo hdparm -tT /dev/nvme0n1p2

Resultado:
`/dev/nvme0n1p2:`
 `Timing cached reads:   9144 MB in  2.00 seconds = 4576.47 MB/sec`
 `Timing buffered disk reads: 2658 MB in  3.00 seconds = 885.48 MB/sec`

### Lap HP
`/dev/mapper/ubuntu--vg-ubuntu--lv`

Resultado:
`/dev/mapper/ubuntu--vg-ubuntu--lv:`
 `Timing cached reads:   26312 MB in  2.00 seconds = 13184.55 MB/sec`
 `Timing buffered disk reads: 306 MB in  3.01 seconds = 101.68 MB/sec`
