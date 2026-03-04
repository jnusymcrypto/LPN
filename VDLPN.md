

# Variable-Density Learning Parity with Noise (VDLPN)

>From [2025-FSE-SoK On Shallow Weak PRFs](https://tosc.iacr.org/index.php/ToSC/article/view/12472)
>
>From [2020-FOCS-Correlated Pseudorandom Functions from Variable-Density LPN](https://eprint.iacr.org/2020/1417)

VDLPN 是一个 point function (除了 $f_a(a)=1$ 之外, 其余位置 $f_a(x\neq a)=0$).

VDLPN 的形式化定义为:

$$
F_k(x) := \bigoplus_{i=1}^D \bigoplus_{j=1}^w \prod_{\ell=1}^i (x_{i,j,\ell} \oplus k_{i,j,\ell})
$$
