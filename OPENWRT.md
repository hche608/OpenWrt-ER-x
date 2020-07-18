# er-x-with-openwrt

# 坑
PS prepare a TTL cable

###
if kernel version is too old that will cause er-x fail to boot up.
```bash
- watchdog -
killall: telnetd: no process killed
killall: ash: no process killed
Sending TERM to remaining processes ... dnsmasq ubusd askfirst logd netifd odhcpd ntpd
Sending KILL to remaining processes ...
Performing system upgrade...
[  140.580000] ubi0: attaching mtd5
[  142.940000] ubi0 error: scan_peb: bad image sequence number 939848742 in PEB 1978, expected 1791773879
[  142.960000] Erase counter header dump:
[  142.960000]  magic          0x55424923
[  142.970000]  version        1
[  142.980000]  ec             7
[  142.980000]  vid_hdr_offset 2048
[  142.990000]  data_offset    4096
[  143.000000]  image_seq      939848742
[  143.000000]  hdr_crc        0x42444cfd
[  143.010000] erase counter header hexdump:
[  143.020000] ubi0 error: ubi_attach_mtd_dev: failed to attach mtd5, error -22
ubiattach: error!: cannot attach mtd5
           error 22 (Invalid argument)
1+0 records in
1+0 records out
Unlocking kernel1 ...
```

### how to fix this
1. use TFTP update and TTL cable to the latest kernel first
2. use sysupgrage to update the firmware with UI.