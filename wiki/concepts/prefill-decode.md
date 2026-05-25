---
tags: [概念, 推理架构, 大模型]
created: 2026-05-23
updated: 2026-05-23
sources: 1
---

# Prefill And Decode

## 定义

在大模型推理中，`prefill` 通常负责处理输入上下文、生成首 token，并构建可复用的 KV cache；`decode` 则负责在已有上下文基础上持续生成后续 token。

## 测试意义

- 首 token 更接近 [[llm-performance-testing]] 中 prefill 阶段的表现。
- 吐字率更接近 decode 阶段的表现。
- 如果一个优化理论上只作用于 decode，却显著改善了首 token，测试人员应该优先排查环境、配置或测试脚本问题。

## 常见关联

- KV cache 优化通常更直接影响 prefill。
- MTP、EP 等策略更常被讨论为 decode 侧收益来源。
- [[pd-separation]] 本质上是把这两个阶段拆到不同实例或角色中处理。

## 来源

- [[2025-04-16-llm-performance-testing]]
