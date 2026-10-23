# php/php-src

> 仓库：https://github.com/php/php-src · ⭐ 41,155（2026-10-23 API 实测） · C · License: BSD-3-Clause

**一句话：** PHP 官方解释器源码仓库 —— 全球 80%+ 互联网站点背后的那个 VM 的真身，C 写的引擎 + 扩展系统。

## 核心能力
- **Zend Engine 核心**：C 语言实现的 VM（opcode 循环、内存管理 Zend MM、GC）
- **Zend Extensions API**：一套稳定的 C 扩展接口，OPcache / Redis / Xdebug / Swoole 全部基于它
- **语言运行时**：完整的类型系统（union type / named arguments / enums / fibers / readonly）、JIT（3.10+ opcache JIT）
- **bundled 扩展**：SAPI（mod_php / php-fpm / php-cli）、session、filter、opcache 随源码树分发
- **每年一次大版本**：8.x → 8.4 → 8.5 节奏稳定，2026 年主线为 8.5 分支

## 关键数据（2026-10-23 API 实测）
| 项 | 值 |
|---|---|
| ⭐ Stars | 41,155 |
| 🍴 Forks | 8,310 |
| Open Issues | 2,227 |
| Watchers | 1,357 |
| 创建时间 | 2011-06-16 |
| 最后推送 | 2026-10-22T23:59:52Z |
| 主页 | https://www.php.net |

## 适用场景
- 读源码理解一门语言的 VM 设计（Zend Engine 是最好的教材之一）
- 写 PHP 扩展 / 排查性能问题
- 追踪 PHP 新特性的 RFC 落地与实现细节

## 为什么值得关注
- **工业级语言实现的稀缺样本**：能在生产环境跑了几十年的 C 语言 VM，代码里全是权衡过的细节，JIT、GC、opcode 缓存各有权衡。
- **上游被 8.4/8.5 弃用阴影笼罩之后反而更值得看**：PHP 生态长期受"只会写脚本"的刻板印象影响，但 Zend Engine 的工程量堪比 JVM。读它比读任何教程都直接。
- **BSD-3-Clause**：协议极干净，研究/商用/嵌入都没坑。

## 参考资料
1. [GitHub 仓库](https://github.com/php/php-src)
2. [PHP 官网](https://www.php.net)
3. [PHP 手册](https://www.php.net/manual/zh/)
