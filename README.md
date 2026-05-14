# AdBlock DNS Filters
去广告合并规则，每8个小时更新一次。  
个人收藏了不少广告过滤规则，但是每次往新设备添加的时候很是头疼，于是写了这个项目，定时自动获取各规则源更新，生成合并规则库。

## 说明
1. 定时从上游各规则源获取更新，合并去重。
2. 使用国内、国外各 3 组 DNS 服务，分别对上游各规则源拦截的域名进行解析，去除已无法解析的域名。（上游各规则源中存在大量已无法解析的域名，无需加入拦截规则）
3. 本项目仅对上游规则进行合并、去重、去除无效域名，不做任何修改。如发现误拦截情况，可临时添加放行规则（如 `@@||www.example.com^$important`），并向上游规则反馈。

## 订阅链接
1. 规则x’为规则x的 Lite 版，仅针对国内域名拦截，体积较小（如添加完整规则报错数量限制，请尝试 Lite 规则）
2. 已对 jsdelivr(加速链接1) 缓存进行主动刷新，但仍存在一定刷新延时
3. AdGuard 等浏览器插件使用规则1 + 规则2（规则2为规则1的补充，仅适用浏览器插件）

| 规则 | 原始链接 | 加速链接1 | 加速链接2 | 加速链接3 | 适配说明 |
|:-|:-|:-|:-|:-|:-|
| 规则1 | [原始链接](https://raw.githubusercontent.com/wistone777/adblockfilters/main/rules/adblockdns.txt) | [加速链接1](https://gcore.jsdelivr.net/gh/wistone777/adblockfilters@main/rules/adblockdns.txt) | [加速链接2](https://github.boki.moe/https://raw.githubusercontent.com/wistone777/adblockfilters/main/rules/adblockdns.txt) | [加速链接3](https://ghfast.top/https://raw.githubusercontent.com/wistone777/adblockfilters/main/rules/adblockdns.txt) | AdGuard、AdGuard Home 等 |
| 规则1' | [原始链接](https://raw.githubusercontent.com/wistone777/adblockfilters/main/rules/adblockdnslite.txt) | [加速链接1](https://gcore.jsdelivr.net/gh/wistone777/adblockfilters@main/rules/adblockdnslite.txt) | [加速链接2](https://github.boki.moe/https://raw.githubusercontent.com/wistone777/adblockfilters/main/rules/adblockdnslite.txt) | [加速链接3](https://ghfast.top/https://raw.githubusercontent.com/wistone777/adblockfilters/main/rules/adblockdnslite.txt) | AdGuard、AdGuard Home 等 |
| 规则2 | [原始链接](https://raw.githubusercontent.com/wistone777/adblockfilters/main/rules/adblockfilters.txt) | [加速链接1](https://gcore.jsdelivr.net/gh/wistone777/adblockfilters@main/rules/adblockfilters.txt) | [加速链接2](https://github.boki.moe/https://raw.githubusercontent.com/wistone777/adblockfilters/main/rules/adblockfilters.txt) | [加速链接3](https://ghfast.top/https://raw.githubusercontent.com/wistone777/adblockfilters/main/rules/adblockfilters.txt) | AdGuard 等 |
| 规则2' | [原始链接](https://raw.githubusercontent.com/wistone777/adblockfilters/main/rules/adblockfilterslite.txt) | [加速链接1](https://gcore.jsdelivr.net/gh/wistone777/adblockfilters@main/rules/adblockfilterslite.txt) | [加速链接2](https://github.boki.moe/https://raw.githubusercontent.com/wistone777/adblockfilters/main/rules/adblockfilterslite.txt) | [加速链接3](https://ghfast.top/https://raw.githubusercontent.com/wistone777/adblockfilters/main/rules/adblockfilterslite.txt) | AdGuard 等 |

## 上游规则源
1. 感谢各位广告过滤规则维护大佬们的辛苦付出。

| 规则 | 类型 | 原始链接 | 加速链接1 | 加速链接2 | 加速链接3 | 更新日期 |
|:-|:-|:-|:-|:-|:-|:-|
| adblockdns | dns | [原始链接](https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblockdns.txt) | [加速链接1](https://gcore.jsdelivr.net/gh/wistone777/adblockfilters@main/rules/adblockdns.txt) | [加速链接2](https://github.boki.moe/https://raw.githubusercontent.com/wistone777/adblockfilters/main/rules/adblockdns.txt) | [加速链接3](https://ghfast.top/https://raw.githubusercontent.com/wistone777/adblockfilters/main/rules/adblockdns.txt) | 2026/05/14 |
| adblockfilters | filter | [原始链接](https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblockfilters.txt) | [加速链接1](https://gcore.jsdelivr.net/gh/wistone777/adblockfilters@main/rules/adblockfilters.txt) | [加速链接2](https://github.boki.moe/https://raw.githubusercontent.com/wistone777/adblockfilters/main/rules/adblockfilters.txt) | [加速链接3](https://ghfast.top/https://raw.githubusercontent.com/wistone777/adblockfilters/main/rules/adblockfilters.txt) | 2026/05/14 |
| anti-AD | dns | [原始链接](https://anti-ad.net/easylist.txt) | [加速链接1](https://gcore.jsdelivr.net/gh/wistone777/adblockfilters@main/rules/anti-AD.txt) | [加速链接2](https://github.boki.moe/https://raw.githubusercontent.com/wistone777/adblockfilters/main/rules/anti-AD.txt) | [加速链接3](https://ghfast.top/https://raw.githubusercontent.com/wistone777/adblockfilters/main/rules/anti-AD.txt) | 2026/05/14 |
| Anti-AD | filter | [原始链接](https://anti-ad.net/adguard.txt) | [加速链接1](https://gcore.jsdelivr.net/gh/wistone777/adblockfilters@main/rules/Anti-AD.txt) | [加速链接2](https://github.boki.moe/https://raw.githubusercontent.com/wistone777/adblockfilters/main/rules/Anti-AD.txt) | [加速链接3](https://ghfast.top/https://raw.githubusercontent.com/wistone777/adblockfilters/main/rules/Anti-AD.txt) | 2026/05/14 |
| Anti-AD-加密 DNS | dns | [原始链接](https://raw.githubusercontent.com/privacy-protection-tools/anti-AD/refs/heads/master/discretion/dns.txt) | [加速链接1](https://gcore.jsdelivr.net/gh/wistone777/adblockfilters@main/rules/Anti-AD-加密_DNS.txt) | [加速链接2](https://github.boki.moe/https://raw.githubusercontent.com/wistone777/adblockfilters/main/rules/Anti-AD-加密_DNS.txt) | [加速链接3](https://ghfast.top/https://raw.githubusercontent.com/wistone777/adblockfilters/main/rules/Anti-AD-加密_DNS.txt) | 2026/05/05 |
| Anti-AD-PCDN | dns | [原始链接](https://raw.githubusercontent.com/privacy-protection-tools/anti-AD/refs/heads/master/discretion/pcdn.txt) | [加速链接1](https://gcore.jsdelivr.net/gh/wistone777/adblockfilters@main/rules/Anti-AD-PCDN.txt) | [加速链接2](https://github.boki.moe/https://raw.githubusercontent.com/wistone777/adblockfilters/main/rules/Anti-AD-PCDN.txt) | [加速链接3](https://ghfast.top/https://raw.githubusercontent.com/wistone777/adblockfilters/main/rules/Anti-AD-PCDN.txt) | 2026/05/05 |
| neodevhost | host | [原始链接](https://raw.githubusercontent.com/neodevpro/neodevhost/master/adblocker) | [加速链接1](https://gcore.jsdelivr.net/gh/wistone777/adblockfilters@main/rules/neodevhost.txt) | [加速链接2](https://github.boki.moe/https://raw.githubusercontent.com/wistone777/adblockfilters/main/rules/neodevhost.txt) | [加速链接3](https://ghfast.top/https://raw.githubusercontent.com/wistone777/adblockfilters/main/rules/neodevhost.txt) | 2026/05/13 |

