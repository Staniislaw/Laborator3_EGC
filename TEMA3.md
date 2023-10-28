1.Ce este anti-aliasing? Prezentați această tehnică pe scurt.
anti-aliasing-ul este o tehnică utilizată în grafică pentru a "rotunji"  aspectul aspru al pixelilor care pot apărea la marginile obiectelor sau la detalii fine, cum ar fi punctele,.Un exemplu ar fi daca afisam un punct pe scena sar putea s-al vedem ca patrat il loc de punct.


2.Care este efectul rulării comenzii GL.LineWidth(float)? Dar pentru GL.PointSize(float)? Funcționează în interiorul unei zone GL.Begin()?

GL.LineWidth(float)->seteaza latimea liniilor desenate în OpenGL
GL.PointSize(float)->este folosită pentru a specifica dimensiunea punctelor desenate în OpenGL
si aceste 2 metode nu vor functia in GL.Begin()

3.a)Care este efectul utilizării directivei LineLoop atunci când desenate segmente de dreaptă multiple în OpenGL?
Conectează toate punctele specificate în ordine, desenând o linie de fiecare punct la următorul, iar ultimul punct este conectat înapoi la primul punct, creând o formă închisă.

3.b)Care este efectul utilizării directivei LineStrip atunci când desenate segmente de dreaptă multiple în OpenGL?
mai multe segmente de linie sunt desenate conectând fiecare punct în secvența la următorul. Spre deosebire de LineLoop, nu conectează automat ultimul punct la primul, creând o secvență deschisă de linii.

3.c)Care este efectul utilizării directivei TriangleFan atunci când desenate segmente de dreaptă multiple în OpenGL?
Acesta ia primul punct specific ca centru și îl conectează cu fiecare pereche de puncte ulterioare pentru a forma o serie de triunghiuri în care fiecare punct nou este conectat la punctul central și punctul anterior

3.d)
Care este efectul utilizării directivei TriangleStrip atunci când
desenate segmente de dreaptă multiple în OpenGL?
interpretează punctele specificate ca o serie de triunghiuri conectate.Începând cu primele trei puncte, se creează un triunghi. Fiecare punct suplimentar creează un nou triunghi cu cele două puncte anterioare

4.
De ce este importantă utilizarea de culori diferite (în gradient sau culori selectate per suprafață) în desenarea obiectelor 3D? Care este avantajul?

Exista mai multe avantaje pentru utilizarea culoriilor diferite cum ar fi :  
Accentuarea detaliilor,Iluminare și reflexie,Percepția adâncimii și a formei.

5.
Ce reprezintă un gradient de culoare? Cum se obține acesta în
OpenGL?
Un gradient de culoare implică o tranziție treptată și fluidă între culori.
in OpenGL aceasta se obtine prin  setarea culorile folosind funcția glColor3f() pentru a specifica culorile vârfurilor (punctelor) geometrice


6.Ce efect are utilizarea unei culori diferite pentru fiecare vertex atunci când desenați o linie sau un triunghi în modul strip?
Atunci cand setez pentru fiecare punct o culoare linia va fi reprezentat ca un gradient intre 2 culori  
daca mai setam si o al 3 punct se va continua gradientul cu urmoatoare culoare setata
