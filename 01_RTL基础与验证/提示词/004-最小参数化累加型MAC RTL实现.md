# 第 4 个 ChatGPT 学习提示词：最小参数化累加型 MAC RTL 实现

```text
你是 FPGA RTL 导师。我已经理解 signed/unsigned、补码、乘积位宽、累加器位宽、clear/in_valid，以及 product_valid 与 product_reg 的一拍对齐关系。

现在只学习一个小任务：实现“最小、非流水、参数化、运行累加型 MAC”的 SystemVerilog RTL。不要进入流水线、ready/valid、DMA、量化或 Testbench。

请按下面顺序输出，并在本段结束后停止等待我的回答：
1. 先用几句话明确模块的状态、输入采样条件，以及 rst_n、clear 和 in_valid 同时出现时的优先级。建议约定：rst_n 最高，clear 次之；clear 与 in_valid 同时为 1 时只清零，不累加。
2. 给出一个可综合的模块，参数至少包括 DATA_W、ACC_W，并由 DATA_W 推导 PRODUCT_W。端口包括 clk、rst_n、clear、in_valid、signed a、signed b 和 acc_out。
3. 必须使用 always_ff 与非阻塞赋值保存 accumulator；必须声明明确位宽和 signed 属性的 product 中间变量，并明确说明 product 如何符号扩展到 ACC_W。不要依赖隐式 signed/位宽推导。
4. 代码尽量短小，只实现组合乘法和时序累加；不要加入 product_valid、流水线寄存器、ready/backpressure、饱和、舍入或量化。
5. 给出一个包含 clear、valid=0 和负数乘法的 4 个时钟沿手算例子。
6. 最后只提出 1 个检查问题，然后停止，等待我说“继续”。
```
