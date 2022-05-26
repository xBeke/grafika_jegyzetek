---
title: "Grafika"
author: Beke Ambrus
date: May 24, 2022
geometry: margin=2cm
output: pdf_document
---
# Geometriák és algebrák

## Görék görbülete

$$
a_{cp}=\frac{v^2}{R}
$$

Főgörbületi irányok

$$
K=\kappa_1\kappa_2=a_{min}\cdot a_{max}
$$

## Vektroalgebra

### Összeadás

Eltolás

$$
v=v_1+v_2 (kom,asszoc)
$$

### Kivonás

Egyik vektorból a másikba mutató vektor

$$
v=v_1-v_2
$$

### Skálázás

$$
v_1=\alpha v (dist)
$$

### Skalár szorzat

Egyik vetkor vetülete a másikra * másik hossza

$$
v_1 \cdot v_2 = |v_1||v_2|cos(\alpha)
$$

### Metrika

- $v\cdot v=|v|^2$
- $|v|=\sqrt{v\cdot v}$
- $v^0 = v/ \sqrt{v\cdot v}$
- $v_1\cdot v_2 / |v_1||v_2|=cos(\alpha)$
- Ha két vektor merőleges, a skalárszorzatuk nulla
- Egyik vetkor vetülete a másikra * másik hossza

### Vektor kereszt szorzat

Egyik vektor vetülete a másikra merőleges síkra  
Sakktábla szabály

$$
|v_1\times v_2|=|v_1||v_2|sin(\alpha)
$$

- Nem asszociatív
- Disztributív

$$
v_1 \times v_2 =(x_1e_1+y_1e_2+z_1e_3)\times (x_2e_1+y_2e_2+z_2e_3)=
$$

$$
(y_1z_2-y_2z_1)e_1-(z_2x_1-z_1x_2)e_2+(x_1y_2-x_2y_1)e_3=
$$

$$
\begin {bmatrix}
e_1&e_2&e_3\\
x_1&y_1&z_1\\
x_2&y_2&z_2\\
\end {bmatrix}
$$

## Gradiens
Maximális növekedés iránya és rátája  
Merőleges az irányvektorral

# Differenciál geometria

## Görbület

$$
\frac{N*r''}{r'^2}
$$

# Geometriai modellezés

## Pontok definíciója

## Segítő műveletek
$$
Távolság: |p-q|
$$
$$
Merőleges: p\cdot q=0\\  
$$
$$
Párhuzamos: p\times q=0\\  
$$
$$
Vetület: v^0\cdot p  
$$

## Egyenes

Egyenes implicit egyenlete
$$
n*(r \cdot p)=0
$$
$$
n_x(x-p_x) + n_y(y-p_y)=0
$$
$$
ax+by+c=0
$$

## Kör

Ugyanakkora távolság egy ponttól
$$
|r-c|=R
$$
$$
(x-c_x)^2+(y-c_y)^2-R^2=0
$$

## Ellipszis

Ugyanakkora legyen a távolság összege 2 ponttól (fókuszponttól)
$$
|r-f_1|+|r-f_2|=C
$$

## Hiperbola

Ugyanakkora legyen a távolság külöbsége két ponttól
$$
|r-f_1|-|r-f_2|=C
$$

## Parabola

Azon pontok halamaza, amelynek a ponttól mér távolsága megyezik egy egyenestől mért távolsággal
$$
|r-f|=|n^0\cdot(r-p)|
$$

## Kvadratikus görbék álltalános alakja

$$
f(x,y)=a_{11}x^2+a_{22}y^2+2a_{12}xy+2a_{13}x+2a_{23}y+3a_{33}
$$
$$
f(x,y)=
\begin{bmatrix}
x&y&1
\end{bmatrix}
\begin{bmatrix}
a_{11}&a_{12}&a_{13}\\
a_{21}&a_{22}&a_{23}\\
a_{31}&a_{32}&a_{33}\\
\end{bmatrix}
\begin{bmatrix}
x\\
y\\
1\\
\end{bmatrix}
$$

## Görbék

### Egyenes

- Parametrikus egyenlet  
- Egy állandó sebességű mozgás
$$
x(t)=x_0+v_xt\\
y(t)=y_0+v_yt\\
z(t)=z_0+v_zt\\
$$

### Kör

$$
x(t)=c_x+Rcos(t)\\
y(t)=c_y+Rsin(t)\\
t\in[0,2\pi)
$$

## Szabadformájú görbék

### Lagrange interpoláió

$$ L_i(t)=\frac{\prod_{i\not ={j}}(t-t_j)}{\prod_{i\not ={j}}(t_i-t_j)} $$
$$ r(t)=\sum_iL_i(t)r_i
$$

### Hermite interpoláció

- nem csak helyet adunk meg hanem:
  - Sebesség (r')
  - Gyorsulás (r'')
- Ami a számításhoz kell:
  - $t_i$ időpillanat
  - $p_i=r(t_i)$ pont
  - $v_i=\dot{r}(t_i)$ sebesség vektor
  - $t_{i+1}$ időpillanat
  - $p_{i+1}=r(t_{i+1})$ pont
  - $v_{i+1}=\dot{r}(t_{i+1})$ sebesség vektor

$r(t)=a_3(t-t_i)^3+a_2(t-t_i)^2+a_1(t-t_i)+a_0$  
$\dot{r}(t)=3a_3(t-t_i)^2+2a_2(t-t_i)+a_1$


$r(t_i)=a_0=p_i$  
$r(t_i+1)=a_3(t_{i+1}-t_i)^3+a_2(t_{i+1}-t_i)^2+a_1(t_{i+1}-t_i)+a_0=p_{i+1}$  
$\dot{r}(t_i)=a_1=v_i$  
$\dot{r}(t_i+1)=3a_3(t_{i+1}-t_i)^2+2a_2(t_{i+i}-t_i)+a_1=v_{i+1}$

Az egyenletek megoldása:  
$a_0=p_i$  
$a_1=v_i$  
$a_2=\frac{3(p_{i+1}-p_i)}{(t_{i+1}-t_i)^2}-\frac{(v_{i+1}+2v_i)}{t_{i+1}-t_i}$  
$a_3=\frac{2(p_i-p_{i+1})}{(t_{i+1}-t_i)^3}+\frac{(v_{i+1}+v_i)}{(t_{i+1}-t_i)^2}$

### Bezier approximácio

- $B_i(t):$ ne oszcilláljon
$$
B_i(t)=\binom{n}{i}t^i(1-t)^{n-i}
$$
$$
r(t)=\sum_{i=0}^nB_i(t)r_i
$$

### Catmull-Rom spline

$$
v_i=\frac{1}{2} \left(
  \frac{r_{i+1}-r_i}{t_{i+1}-t_i}+
  \frac{r_i-r_{i-1}}{t_i-t_{i-1}}
  \right)$$

## Felületek

- Explicit: $z=h(x,y)$ (magasságmező)  
- Implicit: $f(x,y,z)=0$  
  - Gömb 
    - $(x-c_x)^2+(y-c_y)^2+(z-c_z)^2-R^2=0$
  - Sík
    - $ax+by+cz+d=0$
- Parametrikus
  - $x=x(u,v)$
  - $y=y(u,v)$
  - $z=z(u,v)$
  - Gömb:
    - $x(u,v)=c_x+Rcos(u)sin(v)$
    - $y(u,v)=c_y+Rsin(u)sin(v)$
    - $z(u,v)=c_z+Rcos(v)$
    - $u\in[0,2\pi),v\in[0,\pi)$
    - 
### Implicit felületek

#### Gömb

$|r-c|=R$

#### Henger

$|r-(p+v^0\cdot((r-p)\cdot v^0))|$=R

#### Ellipszoid

$|r-f_1|+|r-f_2|=C$

#### Hiperboloid

$|r-f_1|-|r-f_2|=C$

#### Paraboloid

$|r-f|=|n^0\cdot (r-p)|$

### Álltalános kvadratikus alak

$$
f(x,y,z)=[x,y,z,1]Q
\begin{bmatrix}
x\\
y\\
z\\
1\\
\end{bmatrix}
$$

# Transzformációk

Affin transzformáció
- Párhuzamost ls egyenest tartó
- Eltolás, elforgatás,nyújtás, nyírás, tükrözés

Minden ilyen transzformáció kifejezhető egy mátrix szorzással, amelyben a sorok rendre a bázisvektorok és az origo:

$$
[x,y,1]
\begin{bmatrix}
i'_x&i'_y&0\\
j'_x&j'_y&0\\
o'_x&o'_y&1\\
\end{bmatrix}
=[x',y',1]
$$

## 2D forgatás

$$
[x,y,1]
\begin{bmatrix}
cos(\phi)&sin(\phi)&0\\
-sin(\phi)&cos(\phi)&0\\
0&0&1\\
\end{bmatrix}
=[x',y',1]
$$

## 3D eltolás

$$
[x,y,z,1]
\begin{bmatrix}
1&0&0&0\\
0&1&0&0\\
0&0&1&0\\
v_x&v_y&v_z&1\\
\end{bmatrix}
=[x',y',z',1]
$$

## 3D skálázás

$$
[x,y,z,1]
\begin{bmatrix}
s_x&0&0&0\\
0&s_y&0&0\\
0&0&s_z&0\\
0&0&0&1\\
\end{bmatrix}
=[x',y',z',1]
$$

## Projektív sík

>Homogén koordinátákkal számszerűsíthetjük a végtelent

### Euklidészi pont

$$
(x,y) => [x,y,1]
$$

### Homogén pont

$$
(x,y) => [x\cdot w, y\cdot w, w] = [X,Y,w]
$$

Homogén osztással, visszatérhetünk az Euklidészi térbe:
$$
x=\frac{X}{w}, y=\frac{Y}{w}, w\not ={0}
$$

Ideális pont:
$$
[X,Y,0]
$$
Itt találkoznak a végtelenben az egyenesek

### Projektív egyenes

- Euklideszi egyenes, Descartes koords
  - $n_xx+n_yy+c=0$
- Euklideszi egyenes, homogén koords
  - $n_x\frac{X}{w}+n_y\frac{Y}{w}+c=0$
- Euklideszi egyenes
  - $n_xX+n_yY+cw=0, w \not ={0}$
- Projektív egyenes
  - $n_xX+n_yY+cw=0$
- Projektív egyenes mátrixokkal:
  - $[X,Y,w]\begin{bmatrix}n_x\\n_y\\c\end{bmatrix}=0$

### Metszés és illeszkedés

- Pontokra illeszthető egyenes
  - $p_1\times p_2$
- Egyenesek metszéspontja
  - $l_1\times l_2$
- p ponton átmenő L egyenesre merőleges
  - $p\times L$

## Projektív tér

>Homogén koordinátákkal számszerűsíthetjük a végtelent

### Euklidészi pont

$$
(x,y,z) => [x,y,z,1]
$$

### Homogén pont

$$
(x,y) => [x\cdot w, y\cdot w, z\cdot w, w] = [X,Y,Z,w]
$$

Homogén osztással, visszatérhetünk az Euklidészi térbe:
$$
x=\frac{X}{w}, y=\frac{Y}{w},z=\frac{Z}{w}, w\not ={0}
$$

Ideális pont:
$$
[X,Y,Z,0]
$$
Itt találkoznak a végtelenben az egyenesek

### Egyenes paraméteres egyenlete

$$
[X(t),Y(t),Z(t),w(t)]= [X_1,Y_1,Z_1,w_1](1-t)+[X_2,Y_2,Z_2,w_2]t
$$

### Sík implicit egyenlete:

$$
n_xX+n_yY+n_zZ+dw=0
$$

### Középpontos vetítés

$$
[x,y,z,1]
\begin {bmatrix}
1&0&0&0\\
0&1&0&0\\
0&0&1&1/d\\
0&0&0&0
\end {bmatrix}=[x,y,z,z/d]
$$
És innen homogén osztással megkaphatjuk a descartes koordinátákat

## Kvaterniók
$q=[s,x,y,z] = [s,d] = s+xi+yj+zk$  
Gyakorlatilag egy 4 dimenziós vektor  
$i^2=j^2=k^2=ijk=-1$  
- $ij=k$  
- $ji=-k$  
- $jk=i$  
- $kj=-i$  
- $ki=j$  
- $ik=-j$  

Szorzás
- $[s_1,d_1]\cdot [s_2, d_2]=[s_1s_2-d_1d_2,s_1d_2+s_2d_1+d_1\times d_2]$

Inverz
- $q^{-1}=\frac{[s,-d]}{|q|2}$

Forgatás
- $q = [cos(\alpha /2),dsin(\alpha/2)], |d|=1$
- $q\cdot [0,u]\cdot q^{-1}=[0,v]$
  - v, az u elforgatottja a d körül alpha-val

Pont:  
$z_p=x_p+y_pi=Re^{i\alpha}=Rcos\alpha+iRsin\alpha$

- Eltolás:
  - $z_p'=z_p+z_t$  
- Skálázás:
  - $z_s=s,  z_p'\cdot z_s$  
- Forgatva nyújtás
  - $z_p'\cdot z_s$

# 2D képszintézis
1. Referencia helyzet
2. Vektorizálás
   1. Ponttal szakaszokkal és háromszögekkel közelítünk
3. Modellezési transzformáció (M)
   1. Világ koordináta rendszer
   2. Elviszi a saját helyére az alkazatot
   3. Itt van az ablak is amit innentől kezdve viszünk magunkkal
4. Kamera transzformáció (VP)
   1. (-1,-1)(1,1) sarokpontba tarszformáljuk a kamerát és minden mást is vele
   2. normalizált eszközkoordinátarendszer / vágási koordináta rendszer
5. Vágás
6. nézeti transzformáció
   1. Átmegyünk fizikai képernyő koordináta rendszer
   2. Figyeleme vesszük a képernyő tényleges méretét
7. Raszterizáció
   1. Melyik pixeleket kell beszínezni

## Vektorizáció

### Görbék

Diszkrét pontokra vizsgáljuk a pontok helyét

### Sokszögek

Minden 4+ csúcsú ***egyszerű*** sokszögnek van diagonálja, azaz mindegyik felbontható diagonálok mentén.

#### Fülek

Ha $p_i$ fül, ha $p_{i-1} <-> p_{i+1}$ diagonál  
Szakasz - szakasz metszéssel vizsgálható, h diagonál-e

### Modell

Beállítjuk az éppen vizsgűált objektum helyét orientációját és nagyságát, a korábban már említett, forgatés, eltolás, skálázás műveletekkel.

### View transzformáció

A $(c_x,c_y)$ középpontú kamera ablakot és minden mást az origo-ba transzformálunk.

$$
[x_{world},y_{world},z_{world},1]\begin{bmatrix}
1&0&0&0\\
0&1&0&0\\
0&0&1&0\\
-c_x&-c_y&0&1\\
\end{bmatrix}
=[x_{cam},y_{cam},z_{cam},1]
$$

### Projekció

A $(w_x,w_y)$oldalhosszúságú ablak ra illesztjük a kamera nézetünket, így kapjuk a normalizált eszköz koordináta nézetet (ndc)

$$
[x_{cam},y_{cam},z_{cam},1]\begin{bmatrix}
2/w_x&0&0&0\\
0&2/w_y&0&0\\
0&0&1&0\\
0&0&0&1\\
\end{bmatrix}
=[x_{ndc},y_{ndc},z_{ndc},1]
$$

### Vágás

Félsíkokra vágunk az ablak mind a 4 oldalán.  
Vágás homogén koordinátákkal:  
$-1<x=X/w<1$  
$-1<y=Y/w<1$  
$-1<z=Z/w<1$  

HA $w>0$  
$-w<X<w$  
$-w<Y<w$  
$-w<Z<w$  

HA $w<0$  
$-w>X>w$  
$-w>Y>w$  
$-w>Z>w$  

### Viewport transzmormáció

1. Eltolunk $(0,0)$ és $(2,2)$-be
2. Skálázunk a kívánt ablakméretre
3. Osztunk 2 vel
4. Eltolunk a végleges helyre az ablakon

$x_{pix}=v_w(x_{ndc}+1)/2+v_x$  
$y_{pix}=v_h(y_{ndc}+1)/2+v_y$  
$z_{pix}=(z_{ndc}+1)/2$  

## Raszterizáció

Pixelekkel való közelítés  

Szakasz effektív rajzolás:  
$y(x)=mx+b=y(x-1)+m$

Háromszög raszterizálás
- Pásztázunk
- mekgeressük a beléő meg a kiléő pontot
- közöttük színezzük a háromszöget

# OpenGL

1. Virtuális világ
2. Vektorizáljuk
3. Modell T
4. View T (kamera)
5. Projekció T (kamera)
6. Vágás
7. ViewPort T
8. Raszterizálás
9. Pixel feldolgozá (fragment shader)
10. Rasztertár