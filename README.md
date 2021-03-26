![Build Openwrt img](https://github.com/mingxiaoyu/N1imagebuilder/workflows/Build%20Openwrt%20img/badge.svg)

基于flippy的38+o和55+o打包Phicomm N1的openwrt

N1的openwrt来自我自己的另一个项目[N1Openwrt](https://github.com/mingxiaoyu/N1Openwrt)

# 如何使用

1. fork项目
2. 修改n1img.yml文件 
  * 找到这句 wget  https://github.com/mingxiaoyu/N1Openwrt/releases/download/$version/openwrt-armvirt-64-default-rootfs.tar.gz
  * 修改为 wget [openert的URL]
  * 修改flippy_url 的地址（可选，本仓储使用了flippy 38+o和55+o 的打包镜像）。
3. 点击Actions -> Workflows -> Run workflow -> Run workflow

# N1刷emmc
非54+版升级到54+版，如果一直卡在fdisk失败那里的解决办法：一是再多试几次，如果还不成功，则需要手动清空分区表然后再重试，具体命令:
```
  dd   if=/dev/zero   of=/dev/mmcblk2  bs=512  count=1  &&  sync
```

# 感激
 * [flippy](https://www.right.com.cn/forum/space-uid-285101.html)
 * [coolsnowwolf/Lede](https://github.com/coolsnowwolf/lede)
