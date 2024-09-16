# 数値計算に重要な数学

Python で数値計算などをする場合に必要となった数学の知識についてまとめておきます。
高校数学の範囲から大学数学の範囲になるかと思います。

## 指数関数・対数関数

### 指数関数

$$ y = a^x $$

- $0<a<1$ 減少関数
- $0a=1$ 一定
- $1<a1$ 増加関数

#### 指数関数の重要な式

$$ a^{x_1} \times a^{x_2} = a^{x_1+x_2} $$

$$ a^{x_1} \div a^{x_2} = a^{x_1-x_2} $$

$$ (a^{x_1})^{x_2} = a^{x_1x_2} $$

$$ (ab)^{x_1} = a^{x_1}b^{x_1} $$

### 対数関数

$$ y = log_a x $$

- $0<a<1$ 減少関数
- $0a=1$ 定義されない
- $1<a1$ 増加関数

#### 対数関数の重要な式

$$ \log_a a = 1 $$

$$ \log_a (x_1x_2) = \log_a x_1 + \log_a x_2 $$

$$ \log_a (x_1/x_2) = \log_a x_1 - \log_a x_2 $$

$$ \log_a x_1^{x_2} = x_2\log x_1 $$

$$ \log_a x_1 = \frac{\log_{x_2}{x_1}}{\log_{x_2}{a}} $$

### 指数関数と対数関数の関係

$$ y=\log_a x \Leftrightarrow x=a^y $$

## 0階・1階・2階のテンソル

### スカラー

方向に依存しない量
$$ y, x, a $$

### ベクトル

方向と大きさを持つ
$$ \boldsymbol{a} =
\begin{Bmatrix}
    a_1 \\ a_2 \\ a_3
\end{Bmatrix}$$
ベクトルの大きさ
$$ |a| = \sqrt{a_1^2+a_2^2+a_3^2} $$

### テンソル

方向と方向に対応する量を持つ
$$ \boldsymbol{A} = \begin{bmatrix}
    a_{11} & a_{21} \\
    a_{12} & a_{22} \\
\end{bmatrix} $$

### ベクトルの計算

- 和
$$ \begin{Bmatrix}
  c_1 \\ c_2
\end{Bmatrix} +
\begin{Bmatrix}
  a_1+b_1 \\ a_2+b_2
\end{Bmatrix}$$
- 差
$$ \begin{Bmatrix}
  c_1 \\ c_2
\end{Bmatrix} +
\begin{Bmatrix}
  a_1-b_1 \\ a_2-b_2
\end{Bmatrix}$$

### テンソルの計算

- 和
$$ \begin{bmatrix}
    c_{11} & c_{21} \\
    c_{12} & c_{22} \\
\end{bmatrix} =
 \begin{bmatrix}
    a_{11}+b_{11} & a_{21}+b_{21} \\
    a_{12}+b_{12} & a_{22}+b_{22} \\
\end{bmatrix}
$$

- 差

$$ \begin{bmatrix}
    c_{11} & c_{21} \\
    c_{12} & c_{22} \\
\end{bmatrix} =
 \begin{bmatrix}
    a_{11}-b_{11} & a_{21}-b_{21} \\
    a_{12}-b_{12} & a_{22}-b_{22} \\
\end{bmatrix}
$$

- 積

$\boldsymbol{A}$ を $l$ 行 $m$ 列、$\boldsymbol{B}$を $m$ 行 $n$ 列とすると 積である $\boldsymbol{C}$ は行列となる
$$ c_{ij} = \sum_{k=1}^m a_{ik} b_{kj} $$

$$ \begin{bmatrix}
    a_{11} & a_{21} \\
    a_{12} & a_{22} \\
\end{bmatrix}
 \begin{bmatrix}
    b_{11} & b_{21} \\
    b_{12} & b_{22} \\
\end{bmatrix} =
 \begin{bmatrix}
    a_{11}b_{11}+a_{21}b_{11} & a_{11}b_{21}+a_{21}b_{22} \\
    a_{12}b_{11}+a_{22}b_{12} & a_{12}b_{21}+a_{22}b_{22} \\
\end{bmatrix}
$$

### 転置

$$ \boldsymbol{A}^T = \begin{bmatrix}
    a_{11} & a_{12} \\
    a_{21} & a_{22} \\
\end{bmatrix} $$

$$ (\boldsymbol{A}\boldsymbol{B})^T = \boldsymbol{B}^T\boldsymbol{A}^T $$
### 行列式
2x2 行列の2つのベクトルでできる平行四辺形の面積になる
$$ \det \boldsymbol{A} = |\boldsymbol{A}| = a_{11}a_{22} - a_{12}a_{21} $$

3x3 行列の3つのベクトルでできる平行六面体の体積になる
### 逆行列
$$ \boldsymbol{A}^{-1} =
\frac{1}{\det \boldsymbol{A}}
\begin{bmatrix}
    a_{22} & -a_{12} \\
    -a_{21} & a_{11} \\
\end{bmatrix}
$$

$$ \boldsymbol{A}^{-1}\boldsymbol{A} = \boldsymbol{I} $$

### 対称テンソル

$$ \boldsymbol{A} = \begin{bmatrix}
    a_{11} & a_{21} \\
    a_{12} & a_{22} \\
\end{bmatrix} \rightarrow a_{12} = a_{21} $$
### ベクトルの内積
各成分の積の総和
$$ |\boldsymbol{a}||\boldsymbol{b}|\cos\theta = \boldsymbol{a} \cdot \boldsymbol{b} = Scalor $$
### ベクトルの外積
大きさは二つのベクトルでできる平行四辺形の面積
方向は二つのベクトルでできる面の法線かつ $A$ から $B$ へ右ねじの進む方向となる
$$ |\boldsymbol{a}||\boldsymbol{b}|\sin\theta = \boldsymbol{a} \times \boldsymbol{b} = Tensor $$

### スカラー三重積
三つのベクトルでできる平行六面体の体積を示す
$$ |\boldsymbol{A} \times \boldsymbol{B}||\boldsymbol{C}|\cos\theta = \boldsymbol{C} \cdot (\boldsymbol{A}\times\boldsymbol{B}) $$

## ベクトルの座標変換

## 総和規約
$$  $$
### ダミーインデックス
$$  $$
### フリーインデックス
$$  $$
### クロネッカーデルタ
$$  $$
