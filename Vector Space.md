$\newcommand{\bra}[1]{\left< #1 \right|}$
$\newcommand{\ket}[1]{\left| #1 \right>}$
$\newcommand{\bk}[2]{\left< #1 \middle| #2 \right>}$
$\newcommand{\bke}[3]{\left< #1 \middle| #2 \middle| #3 \right>}$


## **向量空間**
    
定義：向量空間係由兩個集合組成，其中一個集合是由向量 (vectors) $\mathbb{V} = \{\ket{\alpha}, \ket{\beta}, \ket{\gamma},... \}$ 組成，另一個集合是由純量 (scalars) $\mathbb{F} = \{a, b, c, ... \}$ (在量子力學中，通常是複數) 構成。以及兩個二元運算，分別稱為向量加法 (vector addition) 以及純量乘法 (scalar multiplication)，這兩個集合在這兩種運算之下，具備封閉性，且必須滿足下列性質：



**向量加法**

1. 任意兩個向量相加，得到另一個向量 ：

$$ \ket{\alpha} + \ket{\beta} = \ket{\gamma} $$

2. 向量加法具備交換性 (commutative)：

$$ \ket{\alpha} + \ket{\beta} = \ket{\beta} + \ket{\alpha} $$

3. 向量加法具備結合性 (associative)：

$$\ket{\alpha} + (\ket{\beta} + \ket{\gamma}) = (\ket{\alpha} + \ket{\beta}) + \ket{\gamma} $$

4. 存在一個向量$\ket{0}$，稱為零向量 (zero or null vector)，滿足下列性質： 

$$ \ket{\alpha} + \ket{0} = \ket{\alpha}, \,\,\,\,\forall\ket{\alpha}\in\mathbb{V} $$

5. 對$\mathbb{V}$中的每一個向量$\ket{\alpha}$，皆存在一個對應的加法反元數 $\ket{-\alpha}$，使得

$$ \ket{\alpha} + \ket{-\alpha} = \ket{0} $$

**純量乘法**

6. 純量與向量相乘之後，得到另一個向量：

$$ a\ket{\alpha} = \ket{\gamma} $$

7.  純量乘法相對於向量加法，具備分配性 (distributive)：

$$ a(\ket{\alpha} + \ket{\beta}) = a\ket{\alpha} + a\ket{\beta} $$

8. 純量加法對純量乘法具備分配性：

$$ (a+b)\ket{\alpha} = a\ket{\alpha}+b\ket{\alpha} $$

9. 一般的乘法與純量乘法具備結合性：

$$ a(b\ket{\alpha}) = (ab)\ket{\alpha} $$

10. 在$\mathbb{F}$中存在一個元素$1$，使得$ 1\ket{\alpha} = \ket{\alpha}$, 稱為乘法的單位元素。 



上述這種向量符號，是Paul Dirac發明的，通常也稱為ket  vector，之後會用到另一種向量$\bra{\alpha}$，稱為bra vector (不是那個bra，只是拼法剛好一樣)。需要注意的是，在這種表示方法中，$\alpha$只是一個符號，不是一個數值。舉例來說，$\ket{1}$這個表示方法中，$1$並不是代表數值，他只是一個符號，這個向量的值不一定是$1$。



**線性組合、線性相依與線性獨立**


定義：假設有一組向量$S=\{\ket{\alpha}, \ket{\beta}, \ket{\gamma}, ... \}$，以及一組純量$\{a, b, c, ... \}$，則

$$ a\ket{\alpha} + b\ket{\beta} +c\ket{\gamma} + \cdots $$

稱為S的一種線性組合 (linear combination)。



定義：若找得到一組不全為零的係數$\{a, b, c, ... \}$，使得

$$ a\ket{\alpha} + b\ket{\beta} +c\ket{\gamma} + \cdots = \ket{0} $$

則稱$S$為線性相依 (linearly dependent)，反之則稱為線性獨立 (linearly independent)。



線性獨立有另一種等效的說法，亦即：若$a\ket{\alpha} + b\ket{\beta} +c\ket{\gamma} + \cdots = \ket{0} $，則此式成立的唯一解是係數全為零的解，$a=b=c=\cdots = 0$。



定義：若向量空間$\mathbb{V}$中的每一個向量，皆可以寫成$S$的線性組合，則稱$S$生成$\mathbb{V}$，記作span$(S)$=$\mathbb{V}$。若該集合$S$又同時為線性獨立集，則$S$為向量空間的一個基底 (basis)，基底這個集合中的向量個數，稱為$\mathbb{V}$的維度 (dimension)，記作dim$\mathbb{V}$。



假設$\mathbb{V}$的維度為$n$，選擇一組適當的基底$\mathcal{B} = \{\ket{e_1}, \ket{e_2},..., \ket{e_n}\}$，則空間中的任一個向量$\ket{\alpha}$可以唯一地表示為

$$\ket{\alpha} = a_1\ket{e_1} + a_2\ket{e_2} + \cdots + a_n\ket{e_n} $$

其中

$$ (a_1, a_2,..., a_n) = \left\[\begin{array}{c} a_1 \\ a_2 \\ \vdots \\ a_n \end{array}\right\] $$

稱為$\ket{\alpha}$相對於基底$\mathcal{B}$之座標向量 (coordinate vector)，當$\mathcal{B}$選定時，座標向量是唯一的。



Problem：試證明座標向量為唯一。

證明：假設

$$\ket{\alpha} = a_1\ket{e_1} + a_2\ket{e_2} + \cdots + a_n\ket{e_n},$$

且

$$ \ket{\alpha} = b_1\ket{e_1} + b_2\ket{e_2} + \cdots + b_n\ket{e_n}.$$

兩式相減可得：

$$ \ket{0} = (a_1-b_1)\ket{e_1} + (a_2 - b_2)\ket{e_2} + \cdots + (a_n - b_n)\ket{e_n} $$

若其中某一項係數不為零，例如$a_j \ne b_j$，可將上式同除以$a_j - b_j$並移項之後可得：

$$ \ket{e_j} = -\frac{(a_1 - b_1)}{(a_j - b_j)}\ket{e_1} - \frac{(a_2 - b_2)}{(a_j - b_j)}\ket{e_2} - \cdots - \frac{(a_n - b_n)}{(a_j - b_j)}\ket{e_n} $$

此式意味$\ket{e_j}$可以表示為其他$(n-1)$個向量的線性組合，所以$\mathcal{B}$不為基底，此與問題假設矛盾，因此可知所有分量必須相等$a_1 = b_1$, $a_2 = b_3$,..., $a_n = b_n$，亦即座標向量是唯一的。
