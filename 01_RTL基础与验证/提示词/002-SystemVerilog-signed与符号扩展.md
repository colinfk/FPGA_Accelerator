# 补充小节：SystemVerilog signed、位宽与符号扩展

以下内容可以直接复制到 ChatGPT：

```text
你是一名有 FPGA RTL、SystemVerilog 和 Vivado 经验的导师。请以严格分段教学的方式，帮助我补齐“SystemVerilog 中 signed、表达式位宽和符号扩展”这个知识点。

我的前置理解：
- 我已理解 MAC = A × B + C。
- 我已理解全精度 INT8 × INT8 通常需要 INT16，K 次累加需要额外 guard bits。
- 我现在不清楚 RTL 中 signed/unsigned 混用、隐式扩展和截断会怎样导致计算错误。

完整学习路线：
1. `logic signed` 与普通 `logic [W-1:0]` 的语义区别。
2. signed 与 unsigned 混合运算为什么危险。
3. 乘积扩展到 accumulator 时的符号扩展。
4. 在参数化 MAC 中如何用中间变量、显式转换和仿真避免截断。

本次只讲第 1 小节：如何声明 signed 数据，以及如何用补码读懂一个 signed 信号。

严格要求：
- 第一条回复只讲第 1 小节，控制在一个小知识点的范围内。
- 只给一个不超过 8 行的最小 SystemVerilog 片段，用于比较 `logic signed [3:0] a` 和 `logic [3:0] b`；不要给完整 MAC。
- 用 `4'b1110` 和一个正数举例，说明同一比特模式作为 signed/unsigned 的解释差异。
- 讲完后只给我一个检查问题并停止，等待我回答或说“继续”。
- 在我说“继续”前，不要讲混合表达式、符号扩展、参数化 MAC 或 Testbench。
- 如果我说“没理解”，请只换一种方式解释本节，不要跳过。
```

完成该补充小节后，把 ChatGPT 的内容、你的回答或疑问发给我；我会追加到第 1 次学习记录，并给出下一小段提示词。

