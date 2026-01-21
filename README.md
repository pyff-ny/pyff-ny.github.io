About This Repository
This repository is a collection of real-world IT support cases I encountered while studying and practicing IT fundamentals.
Each case follows a consistent troubleshooting approach:
symptom → hypothesis → verification → resolution → takeaway.
The focus is on reliability, clarity, and repeatability, rather than tools or buzzwords.

🧠 How I Approach IT Problems
I use a simple and practical framework in daily troubleshooting:
Observe the symptom from the user’s perspective
Narrow down the layer (User / OS / Hardware / Network)
Form hypotheses and verify with commands or settings
Fix the issue with minimal side effects
Document what matters for future cases

📁 Case Categories
🌐 Network Issues
Case N1 – Can ping IP but cannot resolve domain name (DNS) — 2026-01-20
Case N2 – DNS resolution failure with valid network connectivity — 2026-01-19
🖥️ Hardware Troubleshooting
Case H1 – Printer not responding: systematic hardware isolation — 2026-01-20
💻 Operating Systems (macOS / Linux)
Case OS2 – iMac Bluetooth toggle unresponsive (controller off) — 2026-01-20
Case OS1 – Backup automation with rsync over SSH — 2026-01-19
👤 User / Workflow Issues
Case U1 – Finder sorting confusion: state vs action mismatch — 2026-01-19

🧰 Tools & Skills Used (Secondary)
Command line diagnostics (ping, traceroute, scutil, rsync, ssh)
macOS system settings and logs
Basic networking concepts (DNS, gateway, subnet)
Documentation and case logging

🎯 Why This Repository Exists
I am preparing for entry-level IT support roles (L1/L2),
where reliability, clear communication, and repeatable troubleshooting matter more than flashy solutions.
This repository reflects how I think and work in real support scenarios

目标岗位（IT Support / Helpdesk / Desktop Support）
我的排障方法论（SOP）
我的展示：#Case 清单（6–10个
#通过作品集展示，我要证明三件事：
#我能快速定位问题边界（硬件/网络/OS/用户 四维）
#我能按流程排障并留证据（现象→假设→验证→修复→复盘）
#我能用可复用的速查表/决策树把经验固化（下次更快）

=================================
Case 分类建议（按 A+ 四大类更贴近你当前学习方式）
硬件（2个）
Case H1：笔记本过热/性能抖动（温度、CPU、风扇、散热、后台进程）
Case H2：存储空间异常（Caches/Containers/CloudKit 之类，含清理策略与风险控制）
网络（2个）
Case N1：能 ping IP 不能访问域名（DNS 诊断链）
Case N2：局域网正常无互联网（Gateway/NAT/ISP/路由器 WAN 诊断链）
OS（1–2个）
Case O1：macOS Finder/排序/路径混乱导致“以为没生效”的问题（状态展示 vs 行为指令）
Case O2：终端脚本/环境变量/path 造成命令不可用（zshrc 结构化排查）
用户/流程（1个）
Case U1：用户描述模糊/误操作导致的“看似故障”（提问框架 + 复现 + 教学交付）
这 6 个 Case 组合，对外看起来就是“能上手干活”的证据链。

=================================
三、每个 Case 的标准写法（强烈建议固定格式）
你每个案例按下面 1 页（或 2 页）写，就非常职业化：
Case 标题（可复制）
Case N1｜能 ping IP 但网站打不开｜根因：DNS 解析链路异常
1) 背景与影响（30秒读完）
场景：家庭/办公室/咖啡店；设备：Mac/iPhone/Windows VM；网络：Wi-Fi/有线
影响：无法访问网站、无法登录、办公中断
紧急程度：高/中/低（为什么）
2) 现象与证据（Evidence）
用户描述（原话）
你观察到的事实（可复现步骤）
证据截图/命令输出（最少 2 条）
示例：ping 1.1.1.1 OK、nslookup 域名失败、浏览器报错码等
3) 假设树（Hypothesis）
把可能性按“概率/验证成本”排序（这一步最体现水平）
H1：DNS 服务器不可用 / 解析被劫持
H2：浏览器代理/ VPN/ 防火墙
H3：IPv6/DoH/缓存异常（视情况）
4) 验证步骤（Tests）与结果（Result）
每一步写成可复用 checklist：
Test 1：nslookup / dig 指向不同 DNS
Test 2：切换网络/重启路由/清 DNS 缓存
Test 3：禁用代理/ VPN
并记录：预期结果 vs 实际结果。
5) 修复动作（Fix）
你做了什么（具体到操作路径/命令）
为什么有效（对应上面的根因）
6) 复盘（Postmortem）
根因一句话
本次最关键的判断点
下次如何更快：写成 3 行“速查规则”
7) A+ 对应知识点（Objective Mapping）
例如：2.1 网络排障、DNS、默认网关、端口、802.11 等
（这能把“做题”与“实战”绑在一起，面试官很吃这一套）
8）每个 Case 额外加一张“速查卡”
每个案例输出一张小卡片（你可以放 Obsidian 或导出 PDF）：
速查卡字段：
触发症状（关键词）
一步判断（最短路径）
关键命令/路径
结论分流：如果 A → 做 X；如果 B → 做 Y
这张卡就是你“把经验产品化”的证据。

================
你可以用它自评，也可以让我按它给你打分）
每个 Case 满分 10 分：
边界判断清晰（0–2）：四维定位是否准确
证据充分（0–2）：不是“我觉得”，而是“我测到”
假设排序合理（0–2）：先高概率/低成本验证
步骤可复用（0–2）：别人照着能复现/能排障
复盘产出（0–2）：形成速查规则/避免复发
达到 8 分以上，你的案例就具备“可展示价值”。

======
.
├── _config.yml
├── index.md
├── about.md
├── assets/
│   └── images/
└── _posts/
    ├── 2026-01-19-case-n1-dns.md
    ├── 2026-01-20-case-n2-gateway.md
    └── 2026-01-21-case-h1-overheat.md
每个 Case 写成一篇文章（Markdown），放 _posts/。文件名必须像：
YYYY-MM-DD-标题.md


文章开头加 Front Matter（这决定标题/日期/分类）：
=======
---
layout: post
title: "Case N1 | 能 ping IP 但打不开域名（DNS）"
categories: [APlus, Network]
tags: [DNS, Troubleshooting, Objective-2-1]
---

## 背景与影响
...

## 现象与证据
...

## 假设树
...

## 验证与结果
...

## 修复动作
...

## 复盘
...

## 对应 A+ Objectives
- 2.1 ...
