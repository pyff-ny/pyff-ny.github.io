1) 固化一套 Case Front Matter 模板（避免分类/路径再漂移）
以后每篇 _posts 顶部都用同一模版
---
layout: post
title: "Case N1 - 能 ping IP 但打不开域名（DNS）"
date: 2026-01-20  # 可选；不写就用文件名日期
categories:
  - network        # 三选一：network / hardware / os
tags:
  - aplus-220-1201
  - troubleshooting
  - dns            # 按主题加：dns / dhcp / gateway / wifi / printer / storage / cpu 等
case_id: "N1-01"   # 你自己的编号体系：N/H/O + 序号
objective: "220-1201 2.1"   # 对应 A+ objectives（可写多个，用逗号分隔）
severity: "P3"     # 可选：P1/P2/P3（面试展示很加分）
status: "done"     # 可选：draft / done
---


2) 首页按“考试 Domain + 四维”做信息架构（更像 Portfolio）
你现在是 Network/Hardware
Network
Hardware
OS
User / Process（用户描述、复现、教育交付）

3) 每个 Case 页面的“展示版结构”（统一版式，面试官一眼扫懂）
你可以把每篇 Case 固定成这 7 段（不需要长，关键是一致）：
症状（用户语言）
初始判断（Hypothesis Tree）
验证步骤（Step 1/2/3… + 结果）
根因（Root Cause）
修复（Fix）
复盘（Prevent/Next time）
A+ Objective Mapping（对应知识点）
你已经在 Case N1 里写了 1–3，补齐 4–7 就是“可展示级”。

4) 图片语法统一成 GitHub Pages 可渲染格式（你现在已经有 assets/images 目录了）
以后都用这种写法：

![scutil dns output](/assets/images/scutil-dns.png)

