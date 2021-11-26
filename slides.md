---
# try also 'default' to start simple
theme: seriph
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: https://source.unsplash.com/collection/94734566/1920x1080
# apply any windi css classes to the current slide
class: 'text-center'
# https://sli.dev/custom/highlighters.html
highlighter: shiki
# show line numbers in code blocks
lineNumbers: false
# some information about the slides, markdown enabled
info: |
  ## Slidev Starter Template
  Presentation slides for developers.

  Learn more at [Sli.dev](https://sli.dev)
# persist drawings in exports and build
drawings:
  persist: false
---

# 2组报告

理论力学动力学普遍定理综合应用


<!--
The last comment block of each slide will be treated as slide notes. It will be visible and editable in Presenter Mode along with the slide. [Read more in the docs](https://sli.dev/guide/syntax.html#notes)
-->

---

# 题目

第二个题

<img src="/problem.jpg" class="rounded w-160 abs-tr mt-16 mr-12"/>

<br>
<br>


<!--
You can have `style` tag in markdown to override the style for the current page.
Learn more: https://sli.dev/guide/syntax#embedded-styles
-->

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

---

# 能量解法

第一种

$$
mg\sin30-mgfs\cos30-m_cg\frac{s}{4}+M\frac{s}{2r}=\frac{1}{2}m_AV_A^2+\frac{1}{2}m_BV_C^2+\frac{1}{2}J_0\omega^2+\frac{1}{2}J_C\omega_C^2
$$

辅助方程：


$$

\begin{array}{c}

  T_0=m\rho^2 & \\
  J_C=\frac{1}{6}mr^2 & \\
  \omega_c=\frac{v}{r} & \\
  \omega=\frac{2v}{r} & \\
  v_A=4v


\end{array}


$$

对能量方程两边进行微分和再微分，可得速度和加速度：

$$
v=\sqrt{\frac{124r^2-48\sqrt{3}fr^2}{51r^2+12\rho^2}gs}, \ a=\frac{62r^2-24\sqrt{3}fr^2}{51r^2+12\rho^2}g
$$

---
layout: default
---

# 达朗贝尔方法：

第二种

整体对O点力矩平衡：
$$
-(Fs+ma_1-\frac{1}{2}mg)\cdot 2r+M-M_{I_1}+M_{I_2}+T_3\cdot 3r-(\frac{m}{3}g+\frac{m}{3}a_2+\frac{m}{2}g+\frac{m}{2}a_2)\cdot 2r=0
$$

对整体y方向受力平衡：

$$
(Fs+ma_1-\frac{1}{2}mg)\sin30+F_Dy+T_3-(\frac{m}{3}g+\frac{m}{3}a_2+\frac{m}{2}g+\frac{m}{2}a_2)=0
$$

其中

$$
F_S=\frac{\sqrt(3)}{2}mgf\ (对物块A受力分析) \\
M_{I_1}=J_0\alpha_1=m\rho^2\alpha_1=m\rho^2\frac{a_1}{2r} \\
M_{I_2}=J_C\alpha_2=\frac{1}{2}(\frac{1}{3}mr^2)\alpha_2=\frac{1}{6}mr^2\cdot \frac{a_1}{4r}=\frac{mr}{24}a_1 \\
a_2=\frac{a_1}{4}
$$




---

可解得$T_3$, $a_1$的关系：

$$
(\frac{4}{3}-\sqrt(3)f)mg-(\frac{19}{8}+\frac{\rho^2}{2r^2})\cdot ma_1+3\sqrt(3)+0
$$

再对滑轮重物(C和B)在D点列力矩平衡：

$$
-(\frac{m}{3}g+\frac{m}{3}a_2+\frac{m}{2}g+\frac{m}{2}a_2)r+MI_2+T_3\cdot 2r=0
$$


可得解：

$$
v=\sqrt{\frac{124r^2-48\sqrt{3}fr^2}{51r^2+12\rho^2}gs}, \ a=\frac{62r^2-24\sqrt{3}fr^2}{51r^2+12\rho^2}g
$$

---
class: px-20
---

# 动力学：

第三种方法：

$\alpha$关系：

$$
a_1=\alpha_1\cdot 2r\quad\quad\rightarrow\quad\quad \alpha_1=\frac{a_1}{2r} \\
\alpha_1 r=2a_2 \quad\quad\rightarrow\quad\quad a_2=\frac{a_1}{4}\\
a_2=\alpha_2r\quad\quad\rightarrow\quad\quad \alpha_2=\frac{a_1}{4r}
$$

对滑块A：

$$
F_N=mg\cos30 \\
mg\sin30-F_f-T_3=ma_1 \\
f_f=fF_N\quad\quad (运动学补充方程)
$$

对鼓轮O:

$$
M+T_32r-T_2r=m\rho^2\alpha_1\quad(动量矩定理)
$$

---

对滑轮和重物：

$$
T_2+T_1-\frac{1}{3}mg-\frac{1}{2}mg=(\frac{m}{3}+\frac{m}{2})a_2\quad\quad(质心运动方程)
$$


对滑轮C:

$$
T_2r-T_1r=\frac{m}{3}r^2\cdot dr\quad\quad (动量矩定理)
$$

$T_1$, $T_2$, $T_3$, $a_1$, $a_2$, $\alpha_1$, $\alpha_2$, $F_N$, $F_f$, 9个未知量, 9个方程

可解得：

$$
v=\sqrt{\frac{124r^2-48\sqrt{3}fr^2}{51r^2+12\rho^2}gs}, \ a=\frac{62r^2-24\sqrt{3}fr^2}{51r^2+12\rho^2}g
$$

---
layout: default
---

# 各组员贡献
任务分配

动力学方法和达朗贝尔方法：李响

能量法以及PPT制作及汇报：赵衍龙、曲庆宇
