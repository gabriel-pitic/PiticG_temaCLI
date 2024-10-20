⚫ Ce este un viewport?

	Un viewport reprezintă o zonă dintr-o fereastră în coordonate de ecran pe care este "desenat" conținutul dorit, 2D sau 3D.

⚫ Ce reprezintă conceptul de frames per seconds din punctul de vedere al bibliotecii OpenGL? 

	În OpenGL conceptul de Frames Per Second reprezintă numărul de actualizări cu o nouă imagine(frame) a ecranului în unitatea timp de o secundă.

⚫ Când este rulată metoda OnUpdateFrame()?

	Metoda specificată este rulată de un număr specificat de ori pe secundă, dar înainte de redarea pe ecran a unor elemente grafice.

⚫ Ce este modul imediat de randare?

	Modul imediat de redare este o metodă de a transmite date despre puncte, linii și triunghiuri direct la placa video pentru a fi redate pe ecran. Este o metodă veche și puțin utilizată.

⚫ Care este ultima versiune de OpenGL care acceptă modul imediat?

	Ultima versiune de OpenGL care acceptă modul imediate de randare este OpenGL 3.2, dar doar printr-un profil de compatibilitate.

⚫ Când este rulată metoda OnRenderFrame()?

	Metoda OnRenderFrame() este rulată după metoda OnUpdateFrame(), astfel că după fiecare schimbare în logica sau input-ul aplicației informația vizuală este actualizată.

⚫ De ce este nevoie ca metoda OnResize() să fie executată cel puțin o dată?

	Pentru a asigura afișarea corespunzătoare a graficii ferestrei, metoda trebuie să fie apelată cel puțin o dată. Acest fapt nu poate fi evitat, deoarece inițializarea ferestrei în sine constituie un eveniment de redimensionare.

⚫ Ce reprezintă parametrii metodei CreatePerspectiveFieldOfView() și care este domeniul de valori pentru aceștia?

	Primul parametru, fovy, este unghiul exprimat în radiani (de obicei între 30 și 90 grade sau 0.50 și 1.57 radiani) a câmpului vizual pe axa verticală. Al doilea, aspect, reprezintă rația dintre lățime și înălțime pentru ecran (de obicei 16:9 sau 1.77, poate ajunge până la 1 în cazul unui pătrat). zNear reprezintă distanța față de cameră la care vor fi randate obiecte, pe când zFar reprezintă distanța maximă la care vor fi randate obiecte. Acești doi parametrii variază de obicei între 0.01f și 1.0f pentru zNear și 100.0f și 1000.0f pentru zFar.