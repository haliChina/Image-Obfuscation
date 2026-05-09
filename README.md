# Image-Obfuscation
Encrypt/Decrypt your pictures with a simple algorithm, supports multiple format

## 体验
[在线使用](https://imgobf.userhali.com)
或下载index.html并双击打开

## 原理
**以下内容由AI总结**
1. Gilbert 曲线（广义 Hilbert 空间填充曲线）
Hilbert 曲线是一种分形曲线，能以"Z字蛇形但保持空间局部性"的方式，把二维网格里的每个像素恰好访问一次，输出一个像素坐标的有序列表。Gilbert 版本把这推广到任意宽高的矩形（不要求 2 的幂次）。
2. 黄金比例偏移（固定密钥）
偏移量 offset = round((√5−1)/2 × W × H) 是黄金比例乘以像素总数。这不是随机密钥，而是一个确定性、无密钥的固定偏移。
3. 沿曲线的循环移位（置换）
- 加密：把曲线第 i 号位置的像素，搬到曲线第 (i+offset)%n 号位置
- 解密：逆向——把第 (i+offset)%n 的像素搬回 i

## 问题反馈与建议
- [issues](https://github.com/haliChina/Image-Obfuscation/issues)
- admin@userhali.com
