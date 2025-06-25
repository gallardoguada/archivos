

Todos
los
programas
que
se
ejec utaron
hasta
el
momento
requ erían
de
ingreso
de
d atos
para
realizar
determinadas
tareas
y
luego
mostrar
resu ltados
.
Tale s
programas
tienen
un
gran
defecto
y
es
que
los
datos
que
se
cargan
desaparecen
cu ando
el
programa
termina
,
por
lo
tanto
cada
vez
que
se
corra
el
programa
hay
que
cargar
los
datos
nu evamente
.
Esto
ocu rre
deb ido
a
que
los
datos
ingresados
qu edan
guardados
en
memo ria
y
al
terminar
el
programa
todos
los
espacios
de
memoria
reser vados
son
devueltos
al
sistema
operativo
perdien do
tod os
los
datos
que
se
habían
cargado
.
Para
so luc ionar
el
problema
deb ería
existir
una
forma
de
almacenar
los
datos
en
forma
permanente,
por
ejemp lo
en
un
medio
magnético
como
el
disco
rígido
de
tal
forma
de
disp oner
de
la
información
en
cualquier
momento
.


Es
un
conjunto
de
datos
estruct urados
en
una
cole cció n
de
entidades
e lementales
o
básicas
denominadas
registros
que
son
de
igua l
tipo
y
constan
a
su
vez
de
diferentes
entida des
de
nivel
má s
bajos
denominadas
cam pos
.




Esta
clas ificación
hace
referencia
a
la
forma
en
la
cuál
se
interpretan
los
datos ,
se
debe
tener
en
cla ro
que
la
única
form a
de
guardar
datos
en
el
disco
es
en
form ato
binario
.
Todos
los
archivos
tienen
al
final
una
marca
que
indica
el
final
del
archivo
.
Dicha
ma rca
se
conoc e
com o
EOF(
End
Of
File
)
.
En
función
del
tipo
de
ele m ento s
a
alma ce nar,
existen
2
tipos
de
archivos
que
son
:

Archivos
de
texto

Archivos
binarios


Unarchivode texto e s una se cuenciade caracteres.
{
Un
a rchivo
de
texto
contiene
toda
su
info rm aci ón
guardad a
en
b inari o
pero
se
interpreta
como
texto
.
{
Absolutam ente
todo
lo
que
contien e
d ebe
se r
inte rpretado
com o
tex to
,
ya
q ue
cu ando
se
escrib e
el
a rc hivo
,
los
datos
s on
e nviados
como
caracteres
.
{
Los
a rchivos
de
tex to
se
caracte rizan
p o r
ser
plan os,
es
d ecir,
todas
l as
letras
ti enen
el
mism o
formato
y
no
hay
p alabras
subrayadas,
en
negrita,
o
letras
de
distinto
tamaño
o
ancho
.


El
hec ho
de
trabajar
con
arch ivos
binarios
esta
asoc iado
con
el
uso
de
estructuras
,
dado
que
la
forma
mas
simple
de
trabajar
es
cargar
una
estructura
para
luego
escribirla
en
el
archivo
y
de
esa
forma
guardar
los
datos
.
En
un
arch ivo
b in ario
se
guardan
datos
con
distinto
formato
,
es
decir
se
pu eden
guardar
caracteres
mezclados
con
enteros
y
flotantes
.


El
modo
es
una
cadena
de
caracteres
que
indica
el
tipo
del
fichero
(texto
o
bin ario)
y
el
uso
que
se
va
ha
hacer
de
él
lec tu ra,
esc ritura,
añadir
datos
al
final,
etc
.
La
siguiente
tabla
mu estra
los
valores
p erm itid os
para
mod o
.


En
cuanto
a
los
valores
permitidos
para
los
by tes,
se
pue d e
añadir
otro
carácter
a
la
cadena
de
mo do
:
{
t
:
mo do
texto
.
Norma lme nte
es
el
modo
por
defec to
.
Se
suele
omitir
.
{
b
:
mo do
binario
.


En
C
,
to das
la s
operac i ones
que
se
rea liz an
sobre
arc hi vo s
son
hechas
a
tra vés
de
func iones
.
Bási camen te
ex is te n
2
categ orías
de
fu ncio nes
p ara
traba jar
con
archi vos
y
son
las
que
usan

y
las
que
acceden
directamente
al
archivo
.
El
hec ho
de
u ti l iz ar
un
bu f fer
s igni f ica
que
no
se
t iene
acceso
direc to
al
arch i vo
y
q ue
cualquie r
opera ción
q ue
se
de see
reali z ar
(lec tura
o
escr i tura )
va
a
ser
hec h a
sobre
el
buf fer
.
Cuand o
el
b uf fer
se
l le na
o
se
vac ía
se
act ual iz an
l os
da tos
desde
y
hacia
el
archivo
.
Se
debe
tener
en
cuen ta
que
al
usar
las
func io nes
sobre
arch i vo s
es ta mos
tr abajando
con
un
in ter me diari o
que
acce de
al
arch i vo
.
Por
lo
tan to
todos
los
da tos
que
van
al
archi vo
(escr it u ra
)
y
que
vien en
( lec tura )
se
encuentra n
en
mem oria
y
frea d
y
fw rite
toman
o
dejan
esos
datos
en
el
archivo
.


Se
pu ede
conseguir
la
entrada
y
la
salida
de
datos
a
un
arch ivo
a
través
del
uso
de
la
biblioteca
de
fun ciones
.
C
no
tiene
palabras
claves
que
realicen
las
operaciones
de
E/S
.
La
siguiente
tabla
da
un
breve
resu men
de
las
funciones
que
se
pueden
utilizar
.
Se
deb e
inclu ir
la
librería
STDI O
.
H
.


Un
pu ntero
a
un
archivo
es
un
puntero
a
una
información
que
define
el
nombre,
el
estado
y
la
posición
actu al
del
arch ivo
.
En
esen cia
identifica
un
arch ivo
esp ecifico
y
utiliza
la
sec uen cia
asociada
para
d irigir
el
fu ncionamiento
de
las
fu nc iones
de
E/S
con
bu ffer
.
Un
puntero
a
un
arch ivo
es
una
variab le
de
tipo
puntero
al
tipo
FIL E
que
se
define
en
STDIO
.
H
.
Un
programa
nec esita
utilizar
pu nteros
a
arch ivos
para
leer
o
esc ribir
en
los
mismos
.
Para
obtener
una
variable
de
este
tipo
se
utiliza
una
sec uen cia
com o
esta
:
FILE *NombreArchivo 
Ejem plo
:
FILE
*arch
;


Los
punteros
en
el
Lenguaje
C
,
son
variables
que
"
apuntan
"
,
es
decir
que
pos een
la
dirección
de
las
ub icaciones
en
mem oria
de
otras
variables,
y
por
med io
de
ellos
se
tiene
un
métod o
de
acceso
a
todas
ellas
.
Lo s
pu nteros
se
dec laran
u tilizand o
el
operador
*
(asterisco)
entre
el
tipo
y
el
identificador
de
la
variable,
por
ejem plo
:
ch ar
*ptr
;
Con
el
op erado r
*,
se
dec lara
una
variable
como
pu ntero
.
Los
punteros
son
variables
que
almacenen
números
enteros
.
El
tipo
char
indica
que
en
^›ı„ _
se
almacenara
una
dirección
de
una
variable
que
es
de
tipo
ch ar
.


La
función
fopen()
abre
una
sec uen cia
para
que
pueda
ser
utilizada
y
la
aso cia
a
un
archivo
.
Su
prototipo
es
:
FI LE*fopen (constch ar n omb re_arch ivo,costch armod o);
fichero = fopen( nombre
-
fichero, modo);
Do nde
nombre_ archivo
es
un
puntero
a
una
cadena
de
caracteres
que
represe ntan
un
nombre
valido
del
archivo
y
puede
incluir
una
es pec ificac ión
del
directorio
.
La
cadena
a
la
que
apunta
modo
deter m ina
com o
se
abre
el
archivo
.


La
forma
habitu al
de
utilizar
la
instrucción
fopen
es
dentro
de
una
sentencia
condicional
que
permita
conocer
si
se
ha
produ cido
o
no
error
en
la
ape rtu ra,
por
ejem plo
:
FlL E
*fich
;
if
((fich
=
fopen ("nomfich
.
dat",
"r"))
==
NULL )
{
/*
control
del
error
de
apertura
*
/
printf
(
"
Error
en
la
apertura
.
Es
pos ible
que
el
fich ero
no
exista
\
n
")
;
}
El
resu ltado
de
fopen
se
almacena
en
la
variable
fich
y
des pués
se
com p ara
fich
con
NULL
p ara
saber
si
se
ha
produ cido
algún
error
.


FILE * 
datos datos
= 
fopen
~^
v}u„˚’Xˆı _U_„

Otras form asde abrir elarchivo:
datos = 
fopen
~^v}u„˚’Xˆı _ ^Á 
datos  = 
fopen
~^v}u „˚’Xˆı _ ^
datos  = 
fopen
~^v}u „˚’Xˆı _ ^
ra

¿Porqué nose puede abrir unfichero?

No existe el archivo

Discolleno

No mbreincorrec to

Direc torio noválido


YYYYY
int
main ()
{
FI LE*parch ;
if
((
parch
=
fopen
~^
:
\
banco
.
ˆı _U_„

//Se
abre
en
modo
lec tura
if
((
parch
=
fopen
~^W
\
v}X ˆı _U_Á

//Si elmod oanteriordioerror elarch ivo
{  //n oexiste ,porlotantose crea
printf
~^
\
nEl
„Z ]À]˚„ı}_ 
}
fclos e
(
parch
);
Return
0;
}
La
idea
es
abrir
un
archivo
para
leer
,
en
el
caso
de
que
exista
se
trabaja
normalmente
,
pero
si
no
existe
lo
abre
el
segu nd o
fopen
.
De
esta
forma
nos
evitamos
borrar
un
arch ivo
que
existe
y
tiene
datos
.


La
funci ón
fc lose ()
ci er ra
una
secu enci a
que
fue
abier ta
medi ante
una
llamada
a
fopen()
.
Esc rib e
toda
la
infor maci ón
que
todavía
se
en cuentre
en
el
buffer
en
el
disco
y
re aliza
un
ci e rre
form al
d e l
a rchivo
a
nivel
del
sistema
operativo
.
Un
e rror
en
el
cie rre
de
una
s ecu en cia
pued e
gene rar
tod o
tipo
de
probl emas,
incluyendo
la
pé rdida
de
datos,
d estr ucc ión
de
a rchivos
y
posibles
errores
intermitentes
en
el
programa
.
Todo archi vo que se abre  de be ser cerr ado ant es de 
termi narel programa.


El
proto tip o
de
esta
fun ción
es
:
int  fc lose (FILE *F);
Dond e
F
es
el
pu ntero
al
archi vo
de vuelt o
por
la
ll amada
a
fclose()
.
Si
se
devuel ve
un
valo r
cero
sig ni fica
que
la
op eració n
de
cierre
ha
teni do
éxito
.
Eje mp lo
Intmain ()
{
FILE *p arch ;
](~~›„Z A(}› ˚v~^W
\
\
v }Xˆı _U_„˚vu}ˆ}o˚ ıµ„
› „]vı(~^
\
v„Z ]À} } µ˚ˆ˚]˚ „ı}
if((fclo se (p arch))== 
-
1) //Se  cie rrae larch ivo
› „]vı(~^
\
v’˚› µ ˆ˚ „„˚„Z ]À
e lse
› „]vı(~^
\
v„Z ]À}„˚Æ]ı}’u˚vı˚
return 0;
}


Para
almacenar
datos
en
un
fichero
es
necesario
realizar
una
operación
de
esc ritura,
de
igual
forma
que
para
obtener
datos
hay
que
efectu ar
una
operación
de
lectura
.
En
C
existen
muc has
y
variadas
operaciones
para
leer
y
esc ribir
en
un
arch ivo
.
Se
pude
mencionar
:
{
fread 
-
f write,
{
fgetc
-
fp utc,
{
fgets
-
fp uts ,
{
fscanf
t
fp rintf
Es
aconsej able
utilizarlas
por
p arej as
;
es
dec ir,
si
se
escribe
con
f write
se
deb e
leer
con
fread
.
Unavezque elarchivose encuentra abierto se puede empezara 
trabajar para lee roesc ribir.


Para
leer
y
escribir
en
ficheros
que
no
sean
de
texto
las
operaciones
que
se
deb en
utilizar
so n
fread
y
f wr ite
.
El
prototipo
de
la
fu nc ión
de
esc ritura
es
el
siguiente
:
int  
f write
( void* 
o rigen
, size_t 
tamaño
, size_t 
cantidad
, FILE*
arch
)
Dond e:
origen
E sun pu nteroal lugardesdedon dese obtienen los datos  
paraescribir enel archivo
tamaño
E sel tamañoen by tesdel dato q uese vaa escribir
Cantidad
E sla cantidad dedatos delongitud  
tamaño
qu ese vana  
escribir
arch
E sel pu nteroa F ILEasociado al arch ivo


Valor
retornado
:
Devuelve
el
número
de
datos
esc ritos
(
cantida d
)
.
Si
el
valor
retornado
es
me nor
al
que
se
indicó
por
me dio
de
la
variable
cantida d
,
sig nifica
que
hubo
un
error
en
la
es cr itura
.
La
función
f write
to m a
cantida d
de
datos
de
longitud
tamaño
desde
la
direc ción
origen
y
los
escribe
en
el
archivo
asociado
al
puntero
arch
com enzando
desde
la
posición
actual
del
ind icador
de
posic ión
del
archivo
.
Una
vez
que
se
com pletó
la
operación
de
esc ritura
el
indicador
de
posición
es
actualizado
(queda
apuntando
al
lugar
donde
se
puede
esc ribir
el
próximo
dato)
.



in tmain  ()
{
FI LE*parch;

in tcant , lon gi ;
 
:
\
\
prueba
.
 
//Se
a bre
en
modo
e s c ri tura
 
\
 
lo ng i= strlen(texto );
cant= fw rite( texto ,  sizeof( char ) , lo ng i, parch );
// Seescrib e al archivo
if (cant<l on gi )
 
\

else
{
 
\
 
fclo se(parch);
}



#include<s tdio.h>
#include<c onio.h>
#def ineAR CH
"c:
\
\
bin.dat"
struct a{
charnombre[ 10] ;
intedad;
};
intmain()
{
FILE *bin;
st ruct a pers;
clrscr() ;
printf( "
\
nSeva agenerarporprimeravez elarchivo
\
n");
if(( bin=fopen(ARC H,"w b"))==NU LL)
printf( "Elarchivo no puede serabierto");


do
{
printf("
\
nI ng reseelno mbre: ");
gets(pers.no mbre);
prin tf("In gresela edad: ");
scanf("%d", &pers.edad);
fw rite(&pers,sizeof(p ers),1,b in );
prin tf("
\
nPresion e1 para termin ar");
}w hile((g etche())!=1);
fclose(bi n);
return 0;
}
An t es
de
escr i b ir
el
ar ch i vo
se
debe
car gar
el
da to
que
se
de sea
guardar
,
en
nues tro
caso
debem os
cargar
la
es truc tura
.
Una
vez
q ue
se
cargar on
tod os
los
camp os
se
lla ma
a
fw rite
y
se
le
pasa
la
d irecc i ón
de
co mienz o
de
la
es truc t ura
(&pers)
,
el
ta maño
en
b yt es
de
la
es tr uctura
(
se
pue de
escrib ir
di re ctame nte
o
usa r
sizeof )
,
la
ca ntidad
de
es truc tura s
qu e
se
van
a
esc ribir
(se
carg ó
solo
una
por
lo
tan to
se
escr ibe
una )
y
finalmente
el
puntero
que
hace
referencia
al
archivo
.
En
el
caso
que
no
se
desee
es cribir
la
est ruc t ura
en tera
se
d eberán
hacer
2
f w ri te
,
uno
par a
la
edad
y
el
otro
para
el
nombre
.


Para
reali zar
la
lectura
de
un
archi vo
se
utili za
la
función
fread
que
tien e
el
sigu iente
proto tip o
int 
fre ad
(void * 
dest ino
,size_ t 
ta maño
,size_ t 
cant idad
,FILE *
arch
)
Dond e
:
destin o
Es
un
pun tero
al
lug ar
donde
se
va
a
dejar
el
dato
leido
con
fread
tamaño
Es
el
tamaño
en
b ytes
del
dato
a
leer
Canti dad
Es
la
canti dad
de
elementos
de
lon gitud
tamaño
que
se
van
a
leer
arch
Es
el
pu ntero
a
la
est ructur a
FILE
asociad a
al
archi vo
desde
el
que
se
va
a
leer
.


Valor
retorn ado
:
:
D evue lve
el
nú me ro
de
d atos
le idos
(
cantidad
)
.
Si
el
valor
retornad o
es
menor
al
que
se
indicó
p or
me dio
de
la
variable
cantidad
,
significa
que
h ubo
un
e rro r
en
la
le ctu ra
o
que
se
lle gó
al
final
de
arch ivo
.
La
fun ción
fread
lee
de sde
el
archivo
refe re nciado
por
arch
a
p artir
de
la
posición
actual
de l
indicador
de
p osición
,
cantidad
de
e lementos
de
longitud
tamaño
y
deja
los
e le mentos
leidos
en
la
d ire cc ión
de
me moria
in d icada
p or
destino
.
Un a
vez
que
se
completó
la
ope ración
de
lectu ra
se
actualiza
automáticamente
el
ind icador
de
po sición
de l
arch ivo
.
A
d ife ren cia
de
lo
que
ocurre
en
la
e scritu ra
,
se
debe
ve rificar
que
se
re alice
la
le ctu ra
mientras
no
se
h aya
lle gad o
al
final
de l
arch ivo
.
Esta
operación
se
re aliza
p or
med io
de
la
fun ció n
feof
.


#include <st dio.h>
#include <conio.h>
#defineARCH
"c:
\
\
bin.dat"
structa{
char nombre[10];
int edad;
};
int main ()
{
FI LE *bin;
structa pers;
int cant;
clrscr();
if ((bin=f open(ARCH,"rb"))== NULL)
printf ("No se pudo abrir el archivo");


w hile(!feof(bi n))
{
cant=frea d(&pers,siz eof( pers) ,1, bin ) ;
if(cant !=1 )
{
if(feof(bi n) )
break;
else
{
err or("No leyo el ultimo registro");
break;
}
}
printf("
\
n %s
\
t %d" ,pers .no mbre ,pers.e dad );
}
fclose(bin);
getch();
return 0;
}
Despu és
de
hacer
la
lectur a
se
debe
ve r ifi car
que
se
haya
leido
la
canti dad
de
datos
que
se
ind icó
.
Ocurre
que
cuando
no
se
lee
la
cantid ad
de
datos
indicada
pu ede
haberse
alcanzado
el
fin al
de
archi vo
o
se
pud o
haber
prod ucido
un
error
.
Es
por
esto
que
cuand o
se
entra
al
if
que
verifi ca
la
canti dad
,
se
debe
pregun tar
si
se
ll ego
al
fin al
del
archivo
.


Sus
prototi pos
son
:
int fpri ntf (FI LE*F,const char *cadena_de_control,  .. ...);
int fscanf(FI LE*F,const char *cadena_de_control,  . .. ..);
Donde
F
es
un
puntero
al
archivo
devuelto
por
una
llamada
a
fopen()
.
fprintf( )
y
fsc a nf( )
dirigen
sus
operaciones
de
E/S
al
archivo
al
que
apunta
F
.
Estas
funciones
se
comport an
exactam ente
como
prinft()
y
s canf()
discuti das
anteriormente,
excepto
que
operan
sobre
archivo
.


Para
que
lo
es cr it o
con
fprintf
pueda
ser
correct amente
leído
con
fs canf
es
con veniente
que
el
f ormato
en
el
que
se
indican
los
tipos
de
datos
que
se
van
a
leer
o
escribir
sean
similar es
para
ambas
instrucciones,
que
los
tipos
de
datos
esté n
separados,
por
ejemplo,
por
un
blanco
y
que
te ngan
un
fin
de
línea
al
final
.
Ejemplo:
intnum;
charcar,cad [10 ];
FILE *f.
/*apert uradelfichero*/
.....
.....
fs canf (f ,"%d %c %s ", &num,&c ar,cad) ;
fprintf (f,"%d %c %s 
\
n ",num,car,cad) ;
fs canf (f ,"%s %c %d ", cad,&c ar,&num);
fprintf (f ,"%s %c %d 
\
n ",cad,car,num);


El arch ivo  inc luirá los  dato s de la s igui ente  forma :
Nomb re del  alu mno 1 nota
Nombre del al umno2 nota
.....
Algu nas
v ece s
se
nec esi ta
m ani p ula r
p or
sep arad o
el
nom bre
de l
alu mno
y
su
n ota ,
para
est o
es
nec esa rio
separarlo
en
campo s
.
Se
pue de
realiz ar
intro duci end o
cara cte res
del imi ta d ores
e ntre
cam po
y
campo,
por
eje mpl o
:

\
 
Esto gen erara un archi vo de tipo :
Nomb re del  alu mno 1;no ta
Nomb re del  alu mno 2;no ta
.....


Ejemplo:
#include< st dio.h>
int main();
{
FILE *fich;
intedad;

 
fc lose(f ich);
/*modolectura*/
/*lecturadel fichero*/

 
\
 
fc lose(f ich);
/*modoañadir*//*escribirenfichero*/
ret urn0;
}


Los
formatos
de
las
instrucciones
de
lectura
y
escritura
de
son
:
carácter_leido =fgetc (f ichero);
fgetc
lee
un
carácter
del
fichero,
el
carácter
leído
se
almacenará
en
carác te r
leído
.
Cua ndo
se
llega
al
final
del
fichero
devuelve
EOF
.
fputc (car, fichero);
fputc
escribe
el
carácter
car
en
el
fichero
.
De vuelve
el
carác ter
escrito
o
EOF
en
caso
de
error
.


Las
funciones
fgets( )
y
fputs()
pueden
leer
y
escribi r
caden as
a
o
desde
los
archivos
.
Los
prototipos
de
estas
funciones
son
:
char*fputs(char*str, FILE*F);
La
func ión
pu ts ()
esc ribe
la
cadena
a
un
archi vo
esp eci fico
.


ch ar *fgets(c ha r*str, int lon g,FILE *F);
La
función
fgets()
lee
una
cadena
desde
el
archivo
espe cif icado
hasta
que
lee
un
carácter
de
nueva
lí nea
o
longit ud
-
1
caracteres
.
fget s (c adena_ lei da, num_c ar ac te re s, fic hero);
Lee
num_car act ere s
del
fichero
y
los
almac ena
en
caden a_leida
colocando
el
carácter
de
fin
de
cade na
'
\
0
'
en
la
posición
num_caracteres
de
la
cadena
lei da
.


Ejemplo:leer uncarácter delarchivonombres.dat.

charletra;

letra=getc (dat os);
fc lose(dat os);


nombres.dat.



putc(letr a,datos); 
fc lose(dat os);



Ejempl o: 
Programa qu ecopi aun archivo carácter a carácter. Realizar 
las correccio nes qu ecop nsidere p ertinente.


La
función
feof(),
que
determina
cuando
se
ha
alcanzado
el
fin
del
archivo
leye ndo
datos
binarios
.
La
función
ti ene
el
siguiente
prototi po
:
int feof (FILE *F) ;
Su
prototipo
se
encuentr a
en
STDIO
.
H
.
Devuelve
ciert o
si
se
ha
alcanzado
el
final
del
archivo,
en
cualquier
otro
caso,
0
.
Por
supuest o,
se
puede
aplicar
este
método
a
archivos
de
texto
tambi én
.


La
fu nc ión
re mov e( )
borr a
el
archivo
es pec ifi ca do
.
Su
prototipo
es
el
siguiente
:
int remove (char*nombre_ar chivo);
Dev uel v e
ce ro
si
tie ne
éx it o
.
Si
no
un
va lor
dist into
de
cero
.


La
función
fseek
(
)
permite
desp laz ar
el
indicador
de
posición
del
archivo
a
la
posición
que
se
le
indique
.


Valor
de
Ret orn o
:
de vuel ve
un
valor
para
que
el
prog rama
pu eda
control ar
el
correcto
fun cion amiento
.
Este
valor
pu ede
ser
:
0
:
Todo
ha
funcion ado
correctamente
-
1
:
En
ot ro
caso
.
Elproto tip ode l a fun ción es:
int  
fseek
( FILE*
arch
,long 
desplazamiento
, int 
origen
)
Dond e:
arch
Pun tero
a
la
estructura
FILE
asociad a
con
el
archivo
despl azamiento
es
la
canti dad
de
bytes
que
se
despl azará
el
indi cado r
de
po sición
a
partir
de
origen
.
Pueden
ser
:
Positi vo
(movimiento
adelante)Negativo
(movimiento
atrás)
orig en
es
una
constante
que
determina
el
pu nto
de
referencia
a
partir
del
cuál
se
realiza
el
despl azamiento
.


Ejem plo
:
Para
posicionarse
al
comie nzo
del
fichero
:
fse ek (fich , 0L,  0);
Para
posicionarse
al
fina l
del
fich ero
:
fse ek (fich , 0L,  2);
Para
posicionarse
en
otro
pun to
.
Ejem plo
byte
210
.
fse ek (fich , 210 L, 0);
Utilizand o
una
variable
.
long
vari
=
210
L
;
fse ek (fich , vari,  0);
Se
puede
utili za r
auto inc reme ntan do
o
auto dec reme ntan do
:
fse ek (fich , vari+ +, 0);fs eek  (fich , vari
-
-
, 0);


Los
valores
q ue
se
le
pu eden
dar
a
origen
figuran
en
la
sigui ente
tabla
.
Dichos
valores
se
encuentran
defin id os
en
stdio
.
h
SEEK_SET
A
partir
del
comienzo
del
archivo
SEEK_CUR
A
partir
de
la
po sició n
actual
del
archivo
SEEK_END
A
partir
de
el
fin al
del
archivo
Ejemplos
:
fs eek
( 
ptr
,0L , SEEK_ SET )
Mueve
el
i ndicador
de
posición
al
c om ienzo
del
arc hivo
.
El
orig e n
es
SEEK_SET
que
ind ica
el
c o mienzo
del
arc hivo
y
se
d esplaza
0
b yt es
,
por
lo
tanto
queda
al
principio
.
Es
aconsejable
que
cuando
se
desee
llevar
el
indic ador
de
posició n
al
comienzo
del
archiv o
se
utilice
rew in d
ya
que
fs e ek
no
limpia
el
indic ador
de
error
ni
el
de
fin
de
archivo
,
por
lo
tanto
cuando
en
determinada
situación
se
use
fseek
no
va
a
dar
los
resultados
esperados
.


Ejemplos
:
fs eek
(
ptr
,
0
L
,
SEEK_END
)
Mueve
el
indic ador
de
pos ición
al
final
del
ar chivo
.
El
or igen
es
SEE K_END
que
indic a
el
final
del
ar chivo
y
a
par tir
de
alli
se
desplaz a
0
bytes
,
por
lo
tanto
esta
al
final
del
archivo
.
Si
se
desea
en
algún
momento
agregar
datos
,
simplemente
se
debe
usar
esta
función
para
enviar
el
indic ador
de
pos ición
al
final
del
ar ch ivo
.
fs eek
(
ptr
,
20
L
,
SEEK_SET
)
Mueve
el
indic ador
de
pos ición
20
bytes
a
par tir
del
co mienz o
del
ar ch ivo
.
fs eek
(
ptr
,
(long)
(
-
1
)*sizeof
(s truc t
x)
,
SEEK_C UR
)
Mueve
el
indic ador
de
posic ión
una
estructura
para
atras
a
partir
de
la
pos ición
actual
.
Normalmente
esta
forma
se
utiliza
cu ando
se
estan
editando
datos
del
archivo
.
Al
re alizar
una
búsqueda
se
va
leyendo
cada
uno
de
los
datos
del
archivo
por
medio
de
fread,
pero
cuando
encontramos
el
dato
el
indica dor
de
posic ión
del
archivo
es ta
en
el
dato
sig uiente
al
que
quere mos
modificar
,
co n
lo
cu al
al
hac er
fwr ite
para
escr ibirlo
se
modificará
otro
dato
.
Por
lo
tanto
antes
de
escrib ir
se
debe
mover
el
indic ador
de
pos ición
una
es truc tura
par a
atrás
.




Esta
función
permite
llevar
el
indicador
de
posición
al
comienzo
del
archivo
.
El
protot ipo
es
el
siguiente
:
voi d  
re wind
( FILE *
ar ch
)
La
función
rew ind
ubica
el
indicador
de
posición
del
archivo
refe renciado
por
el
puntero
arch
al
principio
y
limpia
los
indicadores
de
fin
de
archivo
y
error
que
se
encuent ran
el
la
est ruct ura
FILE
.
En
la
lectura
y
escritu ra
de
archi vos
el
indicado r
de
po sición
se
actuali za
automáticamen te
,
pero
existen
casos
,
por
ejemplo
en
las
bú squedas
y
modi ficacion es
sobre
archi vos
,
en
los
cuales
se
nec esi ta
mo ve r
el
in di cado r
de
po sición
a
algú n
lu gar
en
particular
.
Para
ello
se
cuenta
con
las
funcion es
fseek
y
rewin d
.
Por
otra
parte
se
cuenta
con
una
fun ció n
que
permite
ob tener
el
lu gar
don de
se
encuentra
el
in di cador
de
po sición
del
archivo
,
esa
fun ción
es
ftell
.


La
función
ftell
permite
obtener
la
posición
actual
del
indicador
de
posición
.
El
protot ipo
es
el
siguiente
:
long  
ft ell
(FILE  * 
ar ch
)
Donde
arch
es
el
puntero
a
la
est ruct ura
FILE
asociada
al
archivo
.
Valor
retornado
:
Si
la
operación
es
exitosa
devue l ve
la
cantidad
de
b yte s
que
h a y
desde
el
commienzo
del
archivo
hasta
el
lugar
en
que
se
encuentra
el
indicador
de
posición
del
archivo
,
en
caso
contra rio
devuelve

1
L
(
-
1
como
tipo
long)
.


Ejemplo
:
Obtener
el
tamaño
de
un
archivo
en
bytes
#include
<stdio
.
h>
#include
<conio
.
h>
#define
ARCH
"c
:
\
\
bin
.
dat"
int
main
()
{
FILE
*bin
;
long
int
cant
;
if
((bin=fopen( ARCH,"r b" ) )==NULL )
{
printf("No
se
pudo
abrir
el
archivo")
;
exit(
1
)
;
}
fseek
(bin
,
0
L
,
SE EK_E ND
)
;
// S e
e nvía
el
indic a dor
de
posi c ión
al
final
de l
a rc hivo
cant=ftell
(bin)
;

\
nEl
archivo
tiene
%
ld
 
;
fclose(bin)
;
getch()
;
return
0
;
}
Term inada
la
d escr ipció n
de
t odas
las
fu ncio nes
que
se
u ti li z ar án
sobre
arc hi vos
,
podemos
escr ibir
2
ejemplos
simples
de
búsqueda
y
modificación
.


Existen
dos
operadores
esp eciales
de
pu nteros
:
*
y
&
.
{
El
operador
&
(operador
dirección ),
aplicado
sobre
el
nom bre
de
una
variable,
devuelve
su
d irec ció n
de
memo ria
.
Coloca
la
dirección
de
memoria
3500
de
la
variable
cont
en
pu nt
y
la
variable
pu ntero
pu nt
está
ub icada
en
la
dirección
4000
.
Esta
dirección
es
una
posición
interna
d el
orden ador
y
no
tien e
que
ver
con
el
valor
de
cont
.
Se
lee
que
pu nt
^„˚]˚
la
dirección
del
Ào}„ _
cont
.


{
El
operador
*
(operador
indirección )
aplicado
sobre
una
variable
de
tipo
pu ntero
permite
acceder
al
dato
al
que
apunta,
es
dec ir,
al
valor
de
la
variable
situada
en
esa
dirección
de
mem oria
.
valt
=
*p u nt
;
Si
punt
contiene
la
d irección
de
me moria
de
la
variable
cont,
enton ces
coloca
el
valor
de
cont
en
valt
.
Eje mp lo,
si
cont
al
inicio
te nía
el
valor
23
,
enton ces,
desp ués
de
esta
asign ación ,
valt
ten drá
el
valor
23
ya
q ue
es
el
valor
guard ado
en
la
p osición
3500
,
q ue
es
la
d ire cc ión
de
me moria
que
asign ó
a
p u nt
.


En
este
sentido,
los
nombres
de
variables
hacen
refe ren cia
directa
a
un
valor
y
los
pu nteros
hacen
refe ren cia
indirecta
a
un
valor
.
La
referenc ia
a
un
valor
a
través
de
un
pu ntero
se
llama
INDI RECCIÓ N
.


Un
puntero
es
una
variable
que
tien e
la
dirección
de
me moria
de
otra
variable
que
contiene
un
valor
La
dirección
es
la
posición
que
ocu pa
en
la
memoria
una
variable,
un
arreglo,
una
cadena,
una
estructura,
un
arch ivo,
otro
p u ntero,
etc
.
Normalmente
las
variables
contienen
valores
esp ecíficos
.
En
cambio,
los
pu nteros
contienen
direcciones
de
variables
que
contienen
valores
esp ecíficos
.
Si
una
variable
contiene
la
dirección
de
otra
variable
entonc es
se
dice
que
:
^o
primera
variable
apunta
a
la
’˚Pµ vˆ _
.


Razones
para
us ar
p u nteros
en
la
creación
de
programas
:
-
Los
pu nteros
proporcionan
los
med ios
mediante
los
cu ales
las
funciones
mod ifican
sus
argumentos
de
llamada
.
-
Se
pu eden
utilizar
para
so portar
las
rutinas
de
asignación
dinámica,
como
pilas,
colas
y
listas
.
Desventajas
del
uso
de
punteros
:

Pued en
provocar
fallos
cu ando
no
estar
bien
inicializados
o
mal
definid os
.


