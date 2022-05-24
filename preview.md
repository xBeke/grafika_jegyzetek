---
title: "Grafika"
author: Beke Ambrus
date: May 24, 2022
geometry: margin=2cm
output: pdf_document
---
# Geometriák és algebrák

## Euklidészi síkgeometria

Pontok  
Vektorok  
Egyenes  

- Paraméteres egyenlet
- Implicit egyenlet
- Távolság
- Szög

## Gömbi geometria

## Hiperbolikus geometria

## Poincaré diszk

## Projektív geometria

## Műveletek vetorokkal
- Összeadás
  - Eltolás
- Kivonás
  - a-b => b-ből a-ba mutató vektor
- Skalárral való szorzás
  - Egyik vetkor vetülete a másikra * másik hossza
- Kereszt szorzat
  - Egyik vektor vetülete a másikra merőleges síkra
  - Sakktábla szabály

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

