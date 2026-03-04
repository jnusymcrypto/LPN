# LPN
About LPNs: the concepts, the properties, the analysis, and more.


# What is LPN?
Learning Parity with Noise (LPN)

选择一个合适的奇偶校验矩阵 $H\in \mathcal{F}_2^{N\times M}$ ($M>N$) 和一个噪声变量 $e\in{\mathcal{F}_2}^M$, $(H,He)$ 的分布是伪随机的, 即, 对于一个均匀随机且与$H$独立的向量 $r\in\mathcal{F}_2^N$ 而言, 攻击者无法区分 $(H,r)$ 与 $(H,He)$.
