# pirated-list

### 通配符 `*`

Clash 的通配符 `*` 一次只能匹配一级域名

`*.baidu.com` 只匹配 `tieba.baidu.com` 而不匹配 `123.tieba.baidu.com` 或者 `baidu.com`

`*`只匹配 localhost 等没有`.`的主机名

### 通配符 `+`

通配符 ＋ 类似 DOMAIN-SUFFIX, 可以一次性匹配多个级别

`＋.baidu.com` 匹配 `tieba.baidu.com` 和 `123.tieba.baidu.com` 或者 `baidu.com`

通配符 `＋` 只能用于域名前缀匹配

### 通配符 `.`

通配符 . 可以一次性匹配多个级别

`.baidu.com` 匹配 `tieba.baidu.com` 和 `123.tieba.baidu.com`, 但不能匹配 `baidu.com`

通配符 `.` 只能用于域名前缀匹配

### 使用示例

使用通配符时，应当使用引号 `' '`或 `" "`将内容包裹起来

```{.yaml linenums="1"}
fake-ip-filter:
- ".lan"
- "xbox.*.microsoft.com"
- "+.xboxlive.com"
- localhost.ptlogin2.qq.com
```
