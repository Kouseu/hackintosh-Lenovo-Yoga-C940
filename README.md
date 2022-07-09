
# hackintosh-Lenovo-Yoga-C940

## 中文版本（English version please drag the website down）

在经过断断续续接近一年的时间左右，终于解决了联想Yoga C940黑苹果95%的问题，现在已经可以当成日常系统使用。

## 声明
此配置由包括我在内的多个人参与完成，该文件不得用于商用，不得以各种形式出售或收取费用，违者保留追究法律责任的权利。

## 安装条件
参见网络上的黑苹果安装教程，在此不做赘述。

### 注意
1、请更换原装固态PM981a，在该固态下就算强行使用恢复版镜像，也会造成超过4G大小的文件读写出错。

2、解锁CFG和设置DVMT到64m。可以通过刷advanced版bios来设置（不建议，比较复杂而且容易出错，建议使用提供的文件）。

修改bios有风险，请提前备份好bios，以免开不了机。

3、设备信息已经删除，请自行在config.plist里添加设备信息。

## 可使用的功能
| 项目   | 说明                     | 状态                           |
|--------|-------------------------------|:----------------------------------|
| 显卡 | i5-1035g4                | 已驱动                |
| 扬声器 | Realtek ALC298                | 两个扬声器全部驱动                |
| 内麦   | 英特尔智音技术                | 未驱动                            |
| 耳机   | 二合一设备                     | 已驱动（包括麦克风）                |
| 固态   | 西数sn-550                    | 请更换原来的固态                  |
| 摄像头 | 英特尔 XHC                    | 已驱动                            |
| USB口  | 1个a口+2个c口                 | 已驱动                            |
| 雷劈3  | 2个c口                        | 已驱动（可能不支持hdmi输出，未测试） |
| WIFI   | AX201                         | 已驱动                            |
| 蓝牙   | AX201                         | 已驱动                            |
| 触摸板 | 略                            | 已驱动                            |
| 触摸板 | 略                            | 已驱动                            |
| 睡眠   | 不支持s3睡眠，采用deepIdle模式 | 已驱动                            |


## 关于热补丁和kext的说明

触摸屏和触摸板的热补丁是我学习编写的，感谢博主GZ小白（https://blog.gzxiaobai.cn）

AppleALC为C940定制版，在经历了好几天的学习之后，终于驱动了双扬声器。感谢DalianSky，紫米大神（十年以前的资料看得我费劲），以及Dalin提供的建议，是他最先驱动了双扬声器，我在此基础上驱动了耳机输出。

USB的补丁和最先的电池热补丁（现在使用ecenabler）由Grenti提供（https://gitter.im/gr4nt81_twitter）

感谢@anthlonreg热补丁教程。https://github.com/daliansky/OC-little/commits?author=athlonreg

注：GPRW睡眠唤醒文件里面有个设备叫RP05，导致一直设备秒醒，折腾了两个星期才找到正确的值（竟然和dsdt里的不一样）




## English version
After nearly a year on and off, 95% of the hackintosh on Lenovo Yoga C940's  was finally realized, and now it can be used as a daily system.

## Declaration
This configuration is completed by many people including me. This file shall not be used for commercial use, sold or charged in various forms and the right to pursue legal responsibility is reserved.

## Installation conditions
See the hackintosh installation tutorial on the Internet, and I won't go into details here.

### Notice
1. Please replace the original SSD PM981a. Even if you forcibly use the recovery version image in this SSD, it will cause errors in reading and writing in files over the size of 4G.

2. Unlock CFG and set DVMT to 64m. It can be set by flashing the advanced version of the bios (not recommended, it is more complicated and error-prone. Use the provided file tool if possible).

Modifying the bios is risky, please back up the bios in advance, so as not to fail to boot.

3. The platform information has been deleted, please add the platform information in config.plist by yourself.

## Available functions
| Items   |     Notes   | Status                          |
|--------|-------------------------------|:----------------------------------|
| Graphics Card | i5-1035g4             |           Working|
| Speaker | Realtek ALC298                | Both speakers working                |
| Dmic   | Intel Smart Sound Audio Technology                |      Not working                       |
| Headphones jack   | 2-in-1                     | Working（including the mirophone）                |
| SSD| WDC SN-550                    | Place replace the original SSD                  |
| Camera | Intel XHC                    | Working                           |
| USB Ports  | 1 Type A+2 Type C Ports                 | Working                            |
| Thunderbolt 3  | 2 Type C Ports                        | Working(maybe not supported for hdmi output, which haven't been tested yet) |
| WIFI   | AX201                         | Working                            |
| Bluetooth   | AX201                         | Working                           |
| Touchpad |                             | Working                            |
| Touch screen |                             | Working                           |
| Sleep   | S3 is not supported and use deepIdle mode instead | working                            |


## Notes on hot patching and kexts

I learned to write the hot patches for the touch screen and touchpad, special thanks to the blogger GZ Xiaobai (https://blog.gzxiaobai.cn)

AppleALC is a customized version for the C940. After several days of learning and searching on every forum, I finally get both speakers working(thanks to God). Special Thanks to DalianSky, Zimi (the information from ten years ago made me struggle), and Dalin's suggestion, who was the first to drive both speakers, and I patch the headphone output on this basis.

Patch for USB and the battery hot patch of the first version (using ecenabler now) by Grenti (https://gitter.im/gr4nt81_twitter)

Thanks @anthlonreg for the hot patch tutorial. https://github.com/daliansky/OC-little/commits?author=athlonreg

Note: There is a device called RP05 in DSDT, which caused the device to wake up in seconds, and it took almost two weeks for me to find the correct value (it is not the same as the one in dsdt). I have patched the customed GPRW.aml for C940.



