# 03 AXI、DMA 与 Zynq

重点记录 AXI4-Lite 控制寄存器、AXI4-Stream ready/valid、AXI Memory-Mapped、DMA 的 MM2S/S2MM、TLAST/TKEEP、PS/PL 和缓存一致性。

阶段目标是完成：DDR → DMA → AXI4-Stream → 自定义 RTL 加速器 → DMA → DDR。

