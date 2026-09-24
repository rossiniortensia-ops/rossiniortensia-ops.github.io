---
title: 2025年公共DNS服务大全：国内外主流DNS完整列表
date: 2025-10-12 16:00:00
updated: 2025-10-12 16:00:00
categories:
  - DNS
tags:
  - DNS
  - 公共DNS
  - DoH
  - DoT
  - 网络安全
keywords: '公共DNS, DNS服务, DoH, DoT, 阿里DNS, 腾讯DNS, Cloudflare DNS, Google DNS, DNS加密'
description: 2025年国内外主流公共DNS服务大全：收录阿里DNS、腾讯DNSPod、114 DNS、360 DNS、Cloudflare、Google DNS、Quad9等服务商，详细列出IPv4地址、DoH和DoT配置方法，附运营商DNS整理。
author: 裕裕裕
reading_time: 6分钟
comments: true
copyright: true
abbrlink: dns-guide
---

# 🌐 2025年公共DNS服务大全：国内外主流DNS完整列表

<!--more-->

本文档整理了国内外主流的公共 DNS 服务，均支持加密的 **DNS-over-HTTPS (DoH)** 和 **DNS-over-TLS (DoT)** 协议，保障您的查询安全与隐私。

## 什么是公共DNS？

公共DNS是由第三方提供的域名解析服务，相比运营商默认DNS，有以下优势：

- 🚀 **解析速度快**：全球CDN加速
- 🔒 **隐私保护**：不记录用户数据
- 🛡️ **安全防护**：拦截恶意网站
- 🌐 **访问稳定**：不受运营商影响

## 📝 使用说明

- **IPv4 / IPv6**：传统的 DNS 地址，适用于路由器或操作系统配置。
- **DoH (DNS over HTTPS)**：通过 HTTPS 443 端口加密 DNS 请求，防止劫持与窃听。
- **DoT (DNS over TLS)**：通过 TLS 853 端口进行加密通信。
- **国内服务**：速度快、延迟低。
- **国外服务**：隐私好，但国内可能有访问不稳定的情况。

---

## 🇨🇳 国内公共 DNS 服务

| 服务商 | 类型 | IPv4 地址 | DoH 地址 | DoT 地址 | 特点 |
|--------|------|-----------|-----------|-----------|------|
| 阿里 DNS | 国内 | 223.5.5.5 / 223.6.6.6 | https://dns.alidns.com/dns-query | dns.alidns.com | 国内解析速度快，稳定性好。 |
| DNSPod (腾讯) | 国内 | 119.29.29.29 / 182.254.116.116 | https://doh.pub/dns-query | dot.pub | 稳定可靠，同时提供安全防护。 |
| 114 DNS | 国内 | 114.114.114.114 / 114.114.115.115 | 暂无 | 暂无 | 传统 DNS，无污染解析。 |
| 360 DNS | 国内 | 101.226.4.6 / 123.125.81.6 | 暂无 | 暂无 | 主打安全防护。 |
| OneDNS | 国内 | 117.50.11.11 / 52.80.66.66 | https://dns.onedns.net/dns-query | dns.onedns.net | 拦截恶意网站、过滤广告。 |

---

## 🌍 国外公共 DNS 服务

| 服务商 | 类型 | IPv4 地址 | DoH 地址 | DoT 地址 | 特点 |
|--------|------|-----------|-----------|-----------|------|
| Cloudflare | 国外 | 1.1.1.1 / 1.0.0.1 | https://1.1.1.1/dns-query | 1.1.1.1 | 速度快，隐私保护强。 |
| Google DNS | 国外 | 8.8.8.8 / 8.8.4.4 | https://dns.google/dns-query | 8.8.8.8 | 全球节点多，可靠性高。 |
| Quad9 | 国外 | 9.9.9.9 / 149.112.112.112 | https://dns.quad9.net/dns-query | dns.quad9.net | 自动屏蔽恶意网站。 |
| OpenDNS | 国外 | 208.67.222.222 / 208.67.220.220 | https://doh.opendns.com/dns-query | 暂无 | 提供内容过滤与家长控制功能。 |

---

## ⚡ 选择建议

1. **日常使用（国内为主）**：推荐使用阿里 DNS 或 DNSPod。
2. **注重安全防护**：推荐 OneDNS 或 Quad9。
3. **注重隐私保护**：推荐 Cloudflare。
4. **需要特定功能（家长控制、过滤）**：选择 OpenDNS。
5. **国外 DNS 可用性**：国内访问可能受干扰，使用前请测试。

---

## 🔧 使用方法

- **Windows/macOS**：在系统网络设置中可直接启用 DoH。
- **浏览器**：Chrome、Firefox、Edge 可在隐私设置中自定义 DoH 服务器。
- **路由器**：OpenWrt / 梅林固件支持全局配置 DoT / DoH。
- **移动设备**：Android 9+ 和 iOS 14+ 支持在“私有 DNS”中配置 DoT 主机名（如 `dns.alidns.com`）。

---

## 🏢 运营商 DNS 服务整理

| 运营商 | IPv4 / IPv6 地址 | 是否支持 DoH / DoT | 备注 |
|--------|------------------|--------------------|------|
| 中国移动 | 211.138.180.2 / 211.138.180.3 / 2409:8088::a | 不支持 | 各省有不同地址，默认分配。 |
| 中国联通 | 202.96.69.38 / 202.96.64.68 / 2408:8888::8 | 不支持 | 明文 DNS，无加密协议。 |
| 中国电信 | 219.141.136.10 / 202.96.128.86 / 240e:4c:4008::1 | 不支持 | 各地不同节点，未提供 DoH / DoT。 |

---

## 📚 参考资料 / 数据来源

- 阿里云 DNS 官方文档：https://alidns.com/
- 腾讯 DNSPod 官方文档：https://www.dnspod.cn/
- OneDNS 官方站点：https://onedns.net/
- Cloudflare Developers：https://developers.cloudflare.com/
- Google Developers DNS：https://developers.google.com/speed/public-dns/
- Quad9 官方：https://www.quad9.net/
- OpenDNS 官方支持：https://support.opendns.com/
- 运营商 DNS 信息来源：Cloud.tencent.com、ipw.cn、ouq.net、toolb.cn、CSDN 博客等（截至 2025 年 10 月）

---

📅 **最后更新：2025 年 10 月 12 日**  
✍️ 作者：裕裕裕  
🔖 本文为原创内容，转载请注明出处。

---

## 相关文章推荐

- [优质小众公共 DNS 服务推荐](https://yu-blog.top/20831/)
