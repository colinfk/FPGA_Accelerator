# 01 RTL 基础与验证

## 目标

把“会写基础 Verilog”推进到“能够独立设计、验证和综合一个 RTL 模块”。

## 建议顺序

1. 参数、signed arithmetic 和位宽增长
2. 流水线、latency、throughput、valid pipeline
3. 参数化 MAC
4. Self-checking Testbench 和 corner case
5. 同步 FIFO
6. 同步 RAM/BRAM inference
7. PE 和 PE Array

## 阶段验收

- 至少 6 个可综合 RTL module
- 每个模块有 self-checking Testbench
- 能解释输入、输出、valid、latency 和 throughput
- 至少一个 RAM 能推断 BRAM
- 能通过综合报告观察 MAC 的 DSP 映射

`学习记录/` 保存实际学习内容，`提示词/` 保存已经使用过或准备使用的 ChatGPT 提示词。

