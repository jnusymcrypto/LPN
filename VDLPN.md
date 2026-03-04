

# Variable-Density Learning Parity with Noise (VDLPN)

>From [2025-FSE-SoK On Shallow Weak PRFs](https://tosc.iacr.org/index.php/ToSC/article/view/12472)
>
>From [2020-FOCS-Correlated Pseudorandom Functions from Variable-Density LPN](https://eprint.iacr.org/2020/1417)

The security 



VDLPN 是一个 point function (除了 $f_a(a)=1$ 之外, 其余位置 $f_a(x\neq a)=0$).

VDLPN 的形式化定义为:

$$
F_k(x) := \bigoplus_{i=1}^D \bigoplus_{j=1}^w \prod_{\ell=1}^i (x_{i,j,\ell} \oplus k_{i,j,\ell})
$$

其安全性基于安全性参数 $\lambda$, 这个安全性参数又对应 3 个参数 $par=\{w=w(\lambda), D, N=2^D\}$, 结合 LPN 的定义 (假设) 理解: 

* 其中 $w$ 是稀疏性参数 (sparsity parameter),  其对应于 **secret** 噪声向量 Noise vector $\stackrel{\rightarrow}{e}$ 与 **public** 矩阵 $H$ 中每一行的非零 **坐标**.
* 其中 $D$ 是分组参数 (block parameter), 对应于矩阵 $H$ 的分组数量.
* 其中 $N$ 是采样数 (#sample), 这里设置为 $2^D$.

对于给定的三种参数形式, 又可分为三类 VDLPN 的假设形式:

* 标准 VDLPN 假设 (VDLPN(par)) 其中每个 $\vec{e_i}$ 和 $H_i$ 的每一行（长度为 $w \cdot 2^i$ ）独立地从 伯努利分布 $\text{Ber}_{\frac{1}{2}}^{w \cdot 2^i}$ 中采样.
* 精确 VDLPN 假设 (xVDLPN(par)), 其中每个 $\vec{e}_i$ 和 $H_i$ 的每一行均匀地从所有长度为 $w \cdot 2^i$ 且恰好有 $w$ 个非零项的向量集合中采样.
* 正则 VDLPN 假设 (rVDLPN(par)), 其中每个 $\vec{e}_i$ 和 $H_i$ 的每一行通过拼接 $w$ 个随机长度为 $2^i$ 的单位向量得到 (即它们被划分为 $w$ 个等长块，每个块中恰有一个随机的 1).

其中 $x_{i,j,l}$ 与 $k_{i,j,l}$ 都是三维变量
