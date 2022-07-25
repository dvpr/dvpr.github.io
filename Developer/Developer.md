# Developer
<br />


### 此网站发送了 Google Chrome 无法处理的杂乱凭据
### Google Chrome: thisisunsafe SSL error bypass

```
Google Chrome浏览器出现：您目前无法访问 XX.XX.XX.XX，因为此网站发送了 Google Chrome 无法处理的杂乱凭据。
```

在chrome该页面上，直接键盘敲入这11个字符：
```
thisisunsafe
```
鼠标点击当前页面任意位置，让页面处于最上层即可输入,输入时是不显示任何字符的，直接输入即可。

<br />

### Surfingkeys 在多个站点禁用
### Disable Surfingkeys on multiple sites

```
settings.blacklistPattern = /.*mail.google.com.*|.*inbox.google.com.*|trello.com|duolingo.com|youtube.com|udemy.com/i;
```

<br />

### Zabbix 故障处理
### Zabbix debug
<br />

```
2022/07/11 02:04:04 [error] 4671#0: *263116 upstream timed out (110: Operation timed out) while reading response header from upstream, client: 172.24.0.2, server: zabbix, request: "POST /api_jsonrpc.php HTTP/1.1", upstream: "fastcgi://unix:/var/run/php5-fpm.sock", host: "zabbix"

[pool www] server reached pm.max_children setting (5), consider raising it
```

set
```
pm = static
pm.max_children = 200
```
in /etc/php5/php-fpm.conf

for 16G RAM server

### 作弊小抄
### Cheat sheet
<br />

##### HTTP 文件类型列表
##### Content-type MIME TYPE list
<br />

| 文件后缀	| MIME TYPE |
| :-----	| :----- | :----- |
| .doc	| application/msword |
| .dot	| application/msword |
| .docx	| application/vnd.openxmlformats-officedocument.wordprocessingml.document |
| .dotx	| application/vnd.openxmlformats-officedocument.wordprocessingml.template |
| .docm	| application/vnd.ms-word.document.macroEnabled.12 |
| .dotm	| application/vnd.ms-word.template.macroEnabled.12 |
| .xls	| application/vnd.ms-excel |
| .xlt	| application/vnd.ms-excel |
| .xla	| application/vnd.ms-excel |
| .xlsx	| application/vnd.openxmlformats-officedocument.spreadsheetml.sheet |
| .xltx	| application/vnd.openxmlformats-officedocument.spreadsheetml.template |
| .xlsm	| application/vnd.ms-excel.sheet.macroEnabled.12 |
| .xltm	| application/vnd.ms-excel.template.macroEnabled.12 |
| .xlam	| application/vnd.ms-excel.addin.macroEnabled.12 |
| .xlsb	| application/vnd.ms-excel.sheet.binary.macroEnabled.12 |
| .ppt	| application/vnd.ms-powerpoint |
| .pot	| application/vnd.ms-powerpoint |
| .pps	| application/vnd.ms-powerpoint |
| .ppa	| application/vnd.ms-powerpoint |
| .pptx	| application/vnd.openxmlformats-officedocument.presentationml.presentation |
| .potx	| application/vnd.openxmlformats-officedocument.presentationml.template |
| .ppsx	| application/vnd.openxmlformats-officedocument.presentationml.slideshow |
| .ppam	| application/vnd.ms-powerpoint.addin.macroEnabled.12 |
| .pptm	| application/vnd.ms-powerpoint.presentation.macroEnabled.12 |
| .potm	| application/vnd.ms-powerpoint.presentation.macroEnabled.12 |
| .ppsm	| application/vnd.ms-powerpoint.slideshow.macroEnabled.12 |
| .zip	| application/zip |
| .tar	| application/x-tar |

<br />

##### 到底有多少个IP
##### How many IPs
<br />

###### 公式
###### Formula
```
IPv4: 2^(64-x)-3
IPv6：2^(128-x)-3
```

<br />

###### 结果
###### Result
```
IPv4:

/32(1)
/31(2)
/30(4)
/29(8)
/28(16)
/27(32)
/26(64)
/25(128)
/24(256)
/23(512)
/22(1024)
/21(2048)
/20(4096)
/19(8192)
/18(16384)
/17(32768)
/16(65536)
/15(131072)
/14(262144)
/13(524288)
/12(1048576)
/11(2097152)
/10(4194304)
/9(8388608)
/8(16777216)


IPv6:

::/128(1)
::/127(2)
::/126(4)
::/125(8)
::/124(16)
::/123(32)
::/122(64)
::/121(128)
::/120(256)
::/119(512)
::/118(1024)
::/117(2048)
::/116(4096)
::/115(8192)
::/114(16384)
::/113(32768)
::/112(65536)
::/111(131072)
::/110(262144)
::/109(524288)
::/108(1048576)
::/107(2097152)
::/106(4194304)
::/105(8388608)
::/104(16777216)
::/103(33554432)
::/102(67108864)
::/101(134217728)
::/100(268435456)
::/99(536870912)
::/98(1073741824)
::/97(2147483648)
::/96(4294967296)
::/95(8589934592)
::/94(17179869184)
::/93(34359738368)
::/92(68719476736)
::/91(137438953472)
::/90(274877906944)
::/89(549755813888)
::/88(1099511627776)
::/87(2199023255552)
::/86(4398046511104)
::/85(8796093022208)
::/84(17592186044416)
::/83(35184372088832)
::/82(70368744177664)
::/81(140737488355328)
::/80(281474976710656)
::/79(562949953421312)
::/78(1125899906842624)
::/77(2251799813685248)
::/76(4503599627370496)
::/75(9007199254740992)
::/74(18014398509481984)
::/73(36028797018963968)
::/72(72057594037927936)
::/71(144115188075855872)
::/70(288230376151711744)
::/69(576460752303423488)
::/68(1152921504606846976)
::/67(2305843009213693952)
::/66(4611686018427387904)
::/65(9.2233720368548E+18)
::/64(1.844674407371E+19)
::/63(3.6893488147419E+19)
::/62(7.3786976294838E+19)
::/61(1.4757395258968E+20)
::/60(2.9514790517935E+20)
::/59(5.9029581035871E+20)
::/58(1.1805916207174E+21)
::/57(2.3611832414348E+21)
::/56(4.7223664828696E+21)
::/55(9.4447329657393E+21)
::/54(1.8889465931479E+22)
::/53(3.7778931862957E+22)
::/52(7.5557863725914E+22)
::/51(1.5111572745183E+23)
::/50(3.0223145490366E+23)
::/49(6.0446290980731E+23)
::/48(1.2089258196146E+24)
::/47(2.4178516392293E+24)
::/46(4.8357032784585E+24)
::/45(9.671406556917E+24)
::/44(1.9342813113834E+25)
::/43(3.8685626227668E+25)
::/42(7.7371252455336E+25)
::/41(1.5474250491067E+26)
::/40(3.0948500982135E+26)
::/39(6.1897001964269E+26)
::/38(1.2379400392854E+27)
::/37(2.4758800785708E+27)
::/36(4.9517601571415E+27)
::/35(9.903520314283E+27)
::/34(1.9807040628566E+28)
::/33(3.9614081257132E+28)
::/32(7.9228162514264E+28)
::/31(1.5845632502853E+29)
::/30(3.1691265005706E+29)
::/29(6.3382530011411E+29)
::/28(1.2676506002282E+30)
::/27(2.5353012004565E+30)
::/26(5.0706024009129E+30)
::/25(1.0141204801826E+31)
::/24(2.0282409603652E+31)
::/23(4.0564819207303E+31)
::/22(8.1129638414607E+31)
::/21(1.6225927682921E+32)
::/20(3.2451855365843E+32)
```