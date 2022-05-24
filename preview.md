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
Távolság: |p-q|\\
Merőleges: p\cdot q=0\\
Párhuzamos: p\times q=0\\
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

# Transzformációk
# 2D képszintézis
# OpenGL és GPU programozás
# Textúrázás
# 3D képszintézis fizikai alapjai
# Sugárkövetés
# 3D Inkrementális képszintézis
# Fraktálok