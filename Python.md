#coding #udemy 
# 0. Paradigma Object-Oriented
Tutti gli oggetti hanno *2 tipi di responsabilità*
##### FARE
>Espresse dai **metodi** _(non si può prelevare dal conto una quantità maggiore del saldo stesso)_
##### CONOSCERE
>Implementate negli **attributi** _(privati)_ di un oggetto, rese disponibili agli altri oggetti tramite i metodi.
  _(Il conto corrente ha responsabilità di conoscere il saldo, l'intestatario, ecc.)_

_____

# 1. Variabili
##### `a = 20`
**20** è l'_oggetto_
**a** è il _nome_
___

###### Nome valido:
>NON inizia con un numero
>NON contiene parole riservate
>Può contenere lettere, numeri, unicode o underscore


###### ref count
Conteggia i **riferimenti** ad un oggetto
>Incrementa quando si aggiunge un riferimento ad un oggetto
>Diminuisce quando si elimina un riferimento allo _stesso oggetto_

___

# 2. Callable Objects
##### `id() #identità del parametro tra parentesi`
##### `type() #classe (tipo) del parametro tra parentesi`
___

# 3. Attributi
##### dot notation
```
x.y
x.y() #in questo caso l'attributo è una funzione
```
>**x** è il _nome_ dell'**oggetto**
>**y** è il _nome_ dell'**attributo**

Ritorna il valore dell'attributo o esegue la funzione dell'attributo
```
x = 'python'
x.upper() #PYTHON

'python'.upper() #PYTHON
```
___

# 4. Basic Data Types
#### none
>**Unica** istanza (oggetto) della _classe Nonetype_
>**Assenza di un valore**
>Se una funzione _non ritorna un valore_, ritorna **none**, cioè l'_assenza di un valore_
____




#### Numeric types
#Immutabili _3 è sempre 3, non può essere 4_
_Possono essere cambiate le variabili (riferimento all'oggetto), ma non il suo valore_

>**INTEGER**
>Numeri _interi_

>**FLOATING-POINT**
>Valore _decimale_

>**BOOLEAN**
>Valori _logici_ (true/false)
###### CONVERSIONE BINARIA `bin()`
Converte un numero int in formato binario
```
x = 100
bin(x)

0b1100100
```
___



___


#### String types `str`
#Immutabili _non posso cambiare i singoli caratteri della stringa una volta che è stata creata_
_Posso copiare parti di una stringa in un'altra stringa_

>SEQUENZA
>Insieme _ordinato_ di elementi

>UNICODE
>I caratteri della stringa devono _appartenere_ al _set unicode_
```
'python' == "python"
a = '' #stringa vuota, comunque valida
```
>BACKSLASH `\`
>Stringe **multilinee** inserendo `\` alla _fine della riga_
```
"In questo modo python sa che \
la stringa prosegue sulla riga successiva"
```
>3 APICI
>Stringa **multilinea** usando `"""`
```
"""Si può scrivere una stringa multilinea anche
usando tre apici, singoli o doppi """
```
>SEQUENZA DI ESCAPE
>`\n #ritorno a capo della stringa`
>`\t #inserimento tab (tabulazione)`
>`\\ #per inserire carattere backslash nella stringa`
>`\' #per inserire il carattere apice nella stringa
>`\" #analogo a sopra`
___


#### f-string 
_interpolazione di stringhe_
>`%-formatting` modulo formatting _(più antico)_
>`str.format()` introdotto con **python 2.6**
###### STRING INTERPOLATION `f-string`
```
titolo = 'Isola misteriosa'
autore = 'Giulio Verne'

f"Titolo: {titolo}, Autore: {autore}.

Titolo:Isola misteriosa,Autore:Giulio Verne
```
Si possono invocare dei **metodi** all'interno delle graffe:
```
f"Titolo: {titolo.upper()}, Autore: {autore}."

Titolo:ISOLA MISTERIOSA, Autore: Giulio Verne
```

___

#### Espressioni ed operazioni
##### Operatori _aritmetici_
```
+ #addizione
- #sottrazione
* #moltiplicazione
/ #divisione floating-point
// #divisione intera
% #modulo
** #esponenziale
- #meno unitario
```
___

##### Operatori _di assegnamento_
```
=
+= # (a += b) equivale ad (a = a+b)
-=
*=
/=
//=
%=
**=
```
___

##### Operatori di _confronto_
_Ritornano una espressione **booleana**_
```
x < y
x > y
x == y
x != y
x >= y
x <= y
```
___

##### Operatori _logici_
Sono sempre **false**:
>`none`
>`false`
>`0` oppure `0.0` _zero di qualunque tipo_
>`''` oppure `()` oppure `[]` _una qualunque sequenza vuota_
>`{}` _un qualunque dizionario vuoto_

Tutti gli altri valori sono sempre **true**
###### `and`
Ritorna _true_ solo se **tutte** le espressioni sono _true_
```
5 < 10 and 7 > 8 
false
```
___

###### `or`
Ritorna _true_ se **almeno una** delle espressioni è _true_
```
5 < 10 or 7 > 8
true
```
___

###### `not`
Ritorna l'**inversione** di una espressione
```
not 5 > 10
true
```
___


___

##### Operatori _su sequenze_
###### indexing `s[0]` `s[n-1]`
Prelevo un _singolo carattere_ da una stringa specificando un offset all'interno di una coppia `[]`
_offset = indice_
>**Primo** offset
>`[0]`

>**Ultimo** offset
>`[n-1]`
```
s = 'python programming'

s[0]
p

s[8]
r
```
___

###### slicing `s[start_stop-1]`
_offset **stop** sempre **escluso**_
```
s = 'python programming'

s[:] #intera stringa

s[1:4]
yth

s[:4]
pyth

s[9:]
ogramming

s[1:12:3] #3 è lo step
yopg

s[-2:] #offset negativi servono per partire dal fondo
ng
```
____


###### concatenazione `t = s + r`
```
s = 'python'
r = 'programming'

t = s + r
python programming
```
___

###### lunghezza `len()`
```
s = 'python'

len(s)
6
```
___

###### minimo `min()`
```
min(s)
h
```
___

###### massimo `max()`
```
max(s)
y
```
___

___

##### Conversioni di tipo
###### intero `int()`
```
int(false)
0

int(true)
1

int(20.5)
20

int('150')
150

int('python')
errore
```
____

###### float `float()`
```
float(false)
0.0

float(true)
1.0

float(20)
20.0

float('150.5')
150.5

float('python')
errore
```
____

###### stringa `str()`
```
str(false)
'false'

str(true)
'true'

str(20)
'20'

str(150.5)
'150.5'

str('python')
errore
```
___

###### boolean `bool()`
```
bool(10)
true

bool(0)
false

bool('python')
true

bool('')
false
```
___

___

___

___

# 5. Strutture di dati
#### Sequenza
_Serie ordinata di elementi, in cui ogni suo elemento è **indicizzato**_
_(Partendo da 0, poi 1, 2, ..)_
Python ha **2 sequenze**:
>**LISTE mutabili**
>Elementi possono essere _aggiunti, modificati, eleminati_

>**TUPLE immutabili**
>Oggetti inizialmente aggiunti nella tupla, sono **fissi**, _non possono cambiare_

___

### Liste `list`
#mutabile
_Tutte le liste che vengono create sono oggetti, quindi istanze della classe **list**_
>metoto **LITERAL**
>`myList = []` equivalente a `myList = list()`
>`myList = [10, 20, 30] #myList è solo il nome, posso chiamarla come voglio`

>offset
```
myList = [10, 20, 30]

myList[1]
20

myList[-1]
30
```
>**lista di lista**
```
myList = [[1,2], [2,3], [6,7]]

myList[1][1]
3
```
>**modificare** un suo elemento
```
myList = [10, 20, 30]
myList[1] = 50

myList
[10, 50, 30]
```
>**slice** di una lista `[:]`
```
myList = [10, 20, 30]

myList[:2]
[10, 20]
```
>**lunghezza** di una lista
```
myList = [10, 20, 30]

len(myList)
3
```
>**inserire elementi** `.insert()`
```
myList = [10, 20, 30]
myList.insert(2, 50) #inserisco 50 nella posizione 2

myList
[10, 20, 50, 30]
```
>**aggiungere** elementi **in coda** `.append()`
```
myList = [10, 20, 30]
myList.append(50)

myList
[10, 20, 30, 50]
```
>**eliminare** un elemento dalla lista `del`
```
myList = [10, 20, 30]
del myList[1]

myList
[10, 30]
```
>**verifica** che un elemento **sia nella lista** `in`
```
myList = [10, 20, 30]

20 in myList
true
```
>**2 nomi, 1 lista** 
>_Se una lista è definita in più modi, qualsiasi modifica ad uno di questi si ripercuote su tutti_
```
myList = [10, 20, 30]
myList2 = myList

myList2[1] = 60

myList
[10, 20, 60]
```
>**copia** gli elementi di una lista nella nuova lista `.copy()`
```
myList = [10, 20, 30]
myList2 = myList.copy()
myList2[1] = 60

myList2
[10, 20, 60]

myList
[10, 20, 30] #invariata
```
____


### Tuple `tuple`
#Immutabili 
```
medaglie = ()
medaglie = tuple()
medaglie = 'oro', 'argento', 'bronzo'
medaglie = ('oro', 'argento', 'bronzo')

medaglie
('oro', 'argento', 'bronzo')
```
>**unpacking**
>_Devono esserci tante variabili quanti gli elementi all'interno della tupla, altrimenti non funziona_
```
medaglie = 'oro', 'argento', 'bronzo'
o, a, b = medaglie

o
oro

a
argento

b
bronzo
```
___

### Dizionario `dict`
#mutabile 
Ordine non definito _(**non** sono delle sequenze)_
Invece dell'ordine numerico, i dizionari usano delle **chiavi** `key` **univoche** che vengono poi associate a dei rispettivi valori `value`

Un **singolo elemento** di un dizionario è costituito da **2 valori**:
>`key`
>`value`

Le chiavi `key` sono di _qualsiasi_ valore, perché **immutabile**
Essendo i dizionari mutabili, gli elementi _(coppie `key` `value`)_ possono essere **inseriti**, **tolti**, **modificati**.
```
myDict = {
	"primo": 10,
	"secondo": 20,
	"terzo": 30
	}
```
>**aggiungere** 
```
myDict["quarto"] = 40`
```
>**eliminare**
```
del myDict["secondo"]
```
>**eliminare _tutto_** `.clear()`
```
miDict.clear()
miDict = {}
```
>**controllo**
```
"terzo" in myDict
```
>**copia** `.copy()`
```
myDict2 = myDict.copy()
```
___




### Insieme `set`
#mutabile 
Un insieme è un dizionario in cui vengono tolti i valori e mantenute solo le `key`
```
mySet = set()
mySet = set([10, 20, 30, 40])
mySet = {10, 20, 30, 40}
mySet = {} #non va bene, starei creando un dizionario vuoto, non un insieme vuoto
```
```
mySet = set()
mySet.add(10)
mySet.add(20)
mySet.add(30)

mySet
{10, 20, 30}
```
___
>Insieme immutabile `frozenset`
 #Immutabili 
```
mySet = frozenset([10, 20, 30])
mySet.add(40)
error
```
___
>**intersezione** `&`
>_Insieme che contiene tutti gli elementi **comuni** tra gli insiemi_
```
mySet = {10, 20, 30, 40}
mySet2 & {30, 40, 50, 60}
mySet & mySet2
{40, 30}
```
>**unione** `|`
```
mySet = {10, 20, 30, 40}
mySet2 = {30, 40, 50, 60}

mySet | mySet2
{10, 20, 30, 40, 50, 60}
```
>**differenza** `-`
>_Tutti gli elementi che appartengono al primo e che **non** appartengono al secondo_
```
mySet = {10, 20, 30, 40}
mySet2 = {30, 40, 50, 60}

mySet - mySet2
{10, 20}
```
>**or esclusivo XOR** `^`
>_Produce un nuovo insieme che contiene tutti gli elementi che sono contenuti o in uno o nell'altro, ma **non** in entrambi_
```
mySet = {10, 20, 30, 40}
mySet2 = {30, 40, 50, 60}

mySet ^ mySet2
{10, 50, 20, 60}
```
___


___

# 6. Strutture di codice
##### Linee di codice
>Noi scriviamo le _linee fisiche (ciò che vediamo)_
>Queste vengono raggruppate da python in _linee logiche_ che son quelle che poi verranno elaborate ed eseguite
```
#Esempio1
s = "python programming lenguage"
print(s) #visualizzo s
```
_2 linee fisiche (terminano quando si va a capo o inizia un commento)_
_Python le interpreta in 2 linee logiche (rapporto 1:1)_
```
#Esempio2
s = "python \
	 programming \
	 lenguage"
print(s)
```
_4 linee fisiche, interpretate da python come 2 linee logiche (1 per assegnamento, 1 per funzione)_
Le linee fisiche **dopo la prima** vengono chiamate **continuation lines**
>**parentesi aperte**
>_Unico caso in cui non serve `\` per andare a capo_
```
t = (1, 2, 3
4, 5, 6)
print(t)
```
>**blocco di codice**
>_Non si utilizzano `{}`, bensì lo **spazio**_
```
inp = input("Inserire un numero: ")
x = int(inp)
if x < 10:
	s = "Numero minore di 10"
	print(s)
```
___

#### Statement _(istruzione)_
```
s = 'python' #assegnazione
print(s) #funzione

s = 'python'; print(s) #si può fare ma è fortemente sconsigliato
```
#### Statement _semplice_
Non contiene altri statement
Unica linea logica
`s = 'python'`
___
#### Statement _composto_
Contiene altri statement
Scomposto in **più linee logiche**
```
if x < 10: #header
	s = "Numero minore di 10"
	print(s)
elif x == 10: #header
	s = "Numero 10"
	print(s)
else: #header
	s = "Numero maggiore di 10"
	print(s)
```
_Contiene una o più clausole, ognuna di queste composta da un header che inizia sempre con una parola chiave di python e termina sempre con un `:`, seguito da una suite_
```
HEADER:
	SUITE
```
___



#### Statement `if`
```
if x < 10:
	print("< 10")
elif x < 20:
	print(">= 10 e < 20")
elif x < 30:
	print(">= 20 3 < 30")
else:
	print(">= 30")
```
```
#QUIZ
s = 'python'
if s < 'r':
	print("primo")
else:
	print("secondo")

#PRIMO corretto, 'python' inizia con 'p' che è alfabeticamente minore di 'r'
```
___


#### Statement `while` _(ciclo, loop)_
`else` facoltativo _(usato poco)_.
Fintantoché l'espressione di while è `true` , si rimane **dentro il loop**.
La suite associata ad `esle` viene sempre eseguita, in _ogni caso_.
```
x = 0
while x < 3:
	print(x)
	x += 1
```
>Loop **infinito**
>`while true`

>**Uscita** loop
>`break`

>**Ripartire** col ciclo
>`continue`

```
while true:
	x = 'Inserire una stringa'
	if x == 'stop':
		break
	if x < 'b': #cioè se la stringa inizia con la lettera a
		continue #non esegue le linee sotto, riparte in testa
	print(x)
```
___



#### Statement `for` _(iterazione)_
`else` viene sempre eseguita, _a meno che non sia stato usato `break` all'interno del `for`_.
Anche in questo ciclo si utilizzano `break` e `continue`.
```
myList = [1,2,3,4]
for i in myList:
	print(i)

1
2
3
4

myString = 'python'
for i in myString:
	print(i)

p
y
t
h
o
n

myDict = {'a': 1, 'b': 2, 'c': 3} #{'chiave': valore}
for i in myDict:
	print(i) #vengono assegnate solo le chiavi ad i

a
b
c
```
>`.values()`
```
myDict é {'a': 1, 'b': 2, 'c': 3}
for i in myDict.values() #metodo della classe dict
	print(i) #ora assegno i valori delle chiavi

1
2
3
```
>`.items()`
```
myDict = {'a': 1, 'b': 2, 'c': 3}
for i in myDict.items()
	print(i) #assegno l'intera coppia

('a': 1)
('b': 2)
('c': 3)
```
___


#### Funzione `range(start, stop, step)`
>**START**
>Facoltativo
>**0** di _default (se non indicato)_

>**STOP**
>Obbligatorio
>**Non compreso**

>**STEP**
>Facoltativo
>**1** di _default (se non indicato)_

```
for i in range(10,16,2):
	print(i)
10
12
14
```
Oggetto **iterabile**, può essere utilizzato all'interno dell'_iterazione `for`_.

###### Esercizio
_Creare una lista di soli numeri **pari fino a 25** con uno statement for in range **da 10 a 30**_.
```
l = [] #creo una lista vuota
for x in range(10,30):
	if (x % 2 == 0) and (x < 25):
		l.append(x)
l
[10, 12, 14, 16, 18, 20, 22, 24]
```
_Si poteva anche usare lo **step** `range(10,30,2)` invece della condizione sul **resto ** `(x % 2 == 0)_.
___

#### List comprehension
A partire da una lista (o qualsiasi oggetto iterabile), ne produce un'altra in un'**unica istruzione** eseguendo un'elaborazione a partire dai dati della lista d'origine.
##### `[expression for item in iterable if condition]`
>`[]` 
>Perché produce una **lista**

>`expression`
>Regola (logica) applicata ad **item** per produrre il valore che poi entra nella lista di destinazione

>`for item in iterable`
>Ciclo che scorre sulla lista iterabile _(d'origine)_ ed ogni singolo elemento lo mette dentro item _(variabile)_

>`if condition`
>Ogni iterazione viene eseguita solo se la condizione è `true`, se falsa passa all'iterazione successiva _(item non riceve quel elemento)_

```
numbers é [1,2,3,4,5,6,7,8,9]
newList = [n*n for n in numbers if n%2==1]

newList
[1, 9, 25, 49, 81]
```
###### Esercizio
_Ricreo l'esercizio precedente_
```
[x for x in range(10,30) if (x%2==0) and (x<25)]

l
[10, 12, 14, 16, 18, 20, 22, 24]
```
____

#### Dict comprehensiom
Creare un dizionario partendo da un qualunque oggetto iterabile
###### `{key_expr: val_expr for item in iterable if condition}
>`{}`
>Perché dizionario _(non lista `[]`)_

>`key_expr: val_expr`
>Crea un elemento **chiave** `key_expr` ed un elemento **value** `val_expr` per l'elemento **item**

```
a = 'python'
b = {k: ord(k) for k in a}

b
{'p': 112, 'y': 121, 't': 116, 'h': 104, 'o': 111, 'n': 110}
```
___

#### Set comprehension 
Crea un insieme a partire da un oggetto iterabile 
###### `{expression for item in iterable if confition}`
Un insieme _**non** accetta **duplicati**_.
```
a = 'doppione'
c = {k for k in a}

c
{'i', 'e', 'p', 'n', 'o', 'd'}
```
___

#### Funzioni
Sono comunque oggetti, ma anche **eseguibili** _(callable object)_
Si **definisce** e si **chiama**
```
def function_name(parameters):
	statements
```
>`def` `:`
>Parola chiave

>`function_name()`
>Nome che diamo all'oggetto funzione e che useremo poi per chiamarla

>`parameters`
>Elenco **opzionale** di nomi che verranno poi assegnati alle esecuzioni ai valori forniti al momento della chiamata della funzione _(argomenti)_

>`suite`
>Blocco di **istruzioni** che compone la funzione
___

#### Parametri
>**POSIZIONALI**
>Indicati con degli identificatori _(nomi)_
```
def myFunc(a, b, c, d):
	print(a, b, c, d)

myFunc(10, 20, 30, 40)
10, 20, 30, 40
```
>**KEYWORD**
>Posso cambiare ordine rispetto alla definizione della funzione
```
def myFunc(a, b, c, d):
	print(a, b, c, d)

myFunc = (b=10, a=20, d=30, c=40)
20, 10, 30, 40
```
>I parametri _posizionali_ **precedono** quelli keyword!
```
def myFunc(a, b, c, d):
	print(a, b, c, d)

myFunc(10, 20, d=30, c=40)
10, 20, 40, 30
```
>**OPZIONALI**
>_identifier == expression_
>Definiscono, oltre al nome del parametro, anche un valore di default
```
myFunc = (a, b, c=3, d=4)
	print(a, b, c, d)

myFunc(10, 20, 30, 40)
10, 20, 30, 40

myFunc(10, 20)
10, 20, 3, 4 #valori default che ho indicato nella definzione della funzione
```
>`*args`
>Raggruppa un numero variabile di argomenti posizionali all'interno di una tupla.
>La funzione potrà ricevere un _numero variabile di argomenti_ che verranno tutti assegnati a questo _unico parametro_ sottoforma di **tupla**
```
def myFunc(*args)
	print(args)

myFunc(1, 2, 3, 4)
(1, 2, 3, 4)

def myFunc (a, b, *args)
	print(a, b, *args)

myFunc(1, 2, 3, 4, 5)
1 2 (3, 4, 5)
```
>`*kwargs*
>Raggruppa un numero variabile di argomenti all'interno di un **dizionario**
>**Chiavi**: nomi dei parametri che forniamo
>**Valori**: valori che abbiamo fornito per i corrispondenti argomenti
```
myFunc(a=1, b=2, c=3)
{'a': 1, 'b': 2, 'c': 3}
```
___



#### Statement `return`
```
def sum(a,b):
	return a+b
```
Se **non definisco nulla dopo** `return`, la funzione _ritorna l'oggetto **none**_.
```
def sum(a,b):
	return
	
none
```
Se **non definisco** `return`, la funzione _ritorna l'oggetto **none**_
```
def sum(a,b)
	c = a+b
	
none
```
___

#### Chiamare una funzione
`function_name(arguments)`
Gli argomenti vengono passati per riferimento alla funzione ed associati a dei parametri.
Cioè se passiamo una variabile come argomento, il suo oggetto viene passato come oggetto alla funzione e quindi associato al parametro corrispondente all'interno della funzione.
>Oggetto passa da argomento a parametro

>Oggetto **MUTABILE** _(numero intero)_
```
def myFunc(x):
	x = 10
	print(x)

y = 20
myFunc(y) #prende dentro la funzione il valore 20
10 #ma alla variabile viene associato il valore 10

print(y)
20 #fuori dalla funzione l'oggetto originario non ha modificato il suo valore
```

>Oggetto **MUTABILE** _(dizionario)_
```
def myFunc(x):
	x['func'] = 10 #chiave func di tipo stringa e le associo 10

d = {'a': 5}
myFunc(d)
print(d)
{'a': 5, 'func':10}
#d è stato mutato, aggiunta dell'elelemento all'interno della funzione
```
###### Esercitazione
_Definire una funzione a 2 parametri (l1, l2) che ritorni la differenza tra due liste, con `l2 = [1,2,3,4,5]`_.
```
def listadiff(l1, l2 = [1,2,3,4,5]): #definisco la funzione
	l = [] #preparo una lista vuota
	for x in l1: #scorro gli elementi della prima lista l1
		if not x in l2: #se l'elemento in l1 non c'è anche in l2
			l.append(x) #lo aggiungo ad l
		return l #infine ritorno l

a = [1,3,6,7]
b = [3,10]
listadif(a,b) #differenza tra a, b
[1, 6, 7]

listadif(a) #differenza tra a, l2
[6, 7]
```
___


#### Funzioni come oggetto
```
def sum(x, y):
	print(x + y)

sum(10,5) #chiamata alla funzione
sum #chiamata all'oggetto
```
>Tutte le funzioni sono **oggetti** della classe **function**
```
type(sum)
<type 'function'>
```
##### Funzioni _NIDIFICATE_
```
def outer(x,y):
	def sum(a,b):
		return a+b
	print(sum(x,y))

outer(10,5)
15
```
>Inserisco la _def_ di un oggetto all'**interno** della _def_ di un altro oggetto
```
def outer():
	def inner(a,b):
		print(a + b)
	return inner
```
>Si può _ritornare_ una funzione **interna** all'esterno della funzione che l'ha creata, attraverso il suo **nome**, quindi l'**oggetto** funzione
```
>>>f = outer()
>>>f(10,5)
15
```
>Associando una variabile ad una funzione _`f = inner()`_ e poi chiamando quella variabile nel modo `f(a,b)` sto indirettamente chiamando la funzione `inner` con i parametri `(a,b)`
___


##### Funzioni come PARAMETRO
```
def sum(a, b):
	print(a + b)
def myFunc(f, x, y):
	f(x, y)
```
>Definisco una funzione _myFunc_ con 3 parametri:
>`f` è un oggetto funzione
>`x, y` valori numerici
>All'interno di myFunc uso il riferimento ottenuto dall'esterno della funzione puntata da `f` , la chiamo _(qualunque funzione sia)_ e le passo i due parametri `x, y`
```
>>> myFunc(sum, 10, 5)
>>> 15
```
___


___
#### Namespace e Scope

##### NAMESPACE
_Mantenere distinti i nomi che diamo agli oggetti in zone diverse del programma per evitare **collisioni**_
>Mappatura che collega dei nomi a degli oggetti
>Namespace **multipli**, a runtime
>Organizzati in una gerarchia
>Cicli di vita differenti
___
##### SCOPE _(contesto)_
>**Area di codice** che determina dal punto di vista del **runtime** di python, quale namespace dev'essere utilizzato per risolvere effettivamente i nomi.
___
##### GERARCHIA LEGB di namespace 
> **4 livelli**
> Local > Enclosed > Global > Built-in
###### LOCAL scope _(interno ad una funzione)_
>Livello **interno** di una funzione
>Gli argomenti e le variabili che si trovano all'interno di una funzione formano il **local namespace**
>**Creato** ogni volta che *chiamo* una certa funzione
>**Rimosso** quando la funzione **ritorna**
```
def sum(x, y):
	c = x + y
	return x
```
>I due parametri `x` ed `y` e la variabile `c` definita all'interno della funzione, formano il **local namespace** della funzione sum
>In questo livello python cerca di capire qual è l'oggetto associato al nome c.
___
###### ENCLOSED scope _(interno ad una funzione)_
>Consente di risalire ai nomi che non sono definiti dalla funzione, ma sono definiti (eventualmente) in una funzione che racchiude la nostra funzione
```
def outer(x):
	y = 20
	def inner():
		print(x+y)
	inner()
```
>La funzione `inner()` sta utilizzando **2 variabili** `x` ed `y`
>Se guardo il _local scope_, non trovo queste due variabili, perché non sono definite nel namespace locale!
>Python non capisce a quali oggetti si riferiscono
>Risale ad un **livello superiore** per vedere se esiste un **enclosed namespace** ed in questo caso lo trova perché c'è una funzione più esterna che racchiude la funzione `inner()` nella quale questi nomi sono associabili a degli oggetti
>`y` è una variabile
>`x` è un parametro della funzione
___




 
###### GLOBAL scope _(sorgente)_
_Supponendo non abbia trovato le associazioni, python sale ancora di un livello, raggiungendo il **global scope**_
>Il **namespace globale** consente di accedere al namespace di _tutti i nomi definiti al livello del file **sorgente**_ nel quale stiamo scrivendo il programma quando questi nomi sono definiti _al di fuori di tutte le funzioni_
```
x = 100
def myFunc(y):
	print(x + y)
```
>Nell'esempio, la variabile x associata all'oggetto intero che vale 100, è una variabile globale perché definita al di fuori di tutte le funzioni che si trovano in questo sorgente.
>Richiamando la funzione, trovo che di questi 2 parametri `x` ed `y`:
>`y` lo risolvo nel livello **locale**
>`x` nel livello **globale**
___

###### BUILT-IN namespace _(predefinito)_
Viene fornito dall'ambiente di runtime di python
>Contiene le **funzioni e gli oggetti predefiniti** di python, come per esempio `print()`


___

___
#### Global e nonlocal
###### Variable hiding
Se una funzione definisce una variabile locale che però è già presente in un livello di gerarchia più alto nel namespace.
Allora la variabile locale nasconde la variabile globale.
>**Viene sempre nascosta la variabile di un livello superiore**
```
x = 100
def myFunc():
	x = 20
	print(x)

>>> myFunc()
20
>>> print(x)
100
```
___
##### Statement `global`
>Aggira il _variable hiding_
```
x = 100
def myFunc():
	global x
	x = 20
	print(x)

>>> myFunc()
20
>>> print(x)
20
```
>La funzione non crea una nuova variabile locale nel proprio namespace con lo stesso nome di quella globale, ma **utilizza direttamente la variabile globale**.
___

##### Statement `nonlocal`
>Aggira il _variable hiding_
```
def outer():
	y = 20
	def inner():
		nonlocal y
		y = 50
		print(y)
	inner()
	print(y)

>>>outer()
50
50 #la funzione inner() ha modificato il valore della variabile di outer()
```
>**Utilizza la variabile di una funzione che contiene la nostra funzione** (se presente)
>_Non andando ad utilizzare la globale!_
___

___
#### Function decorator
**Arricchisce una funzione**
>Un decoratore di una funzione è una funzione lui stesso che prende in input un'altra funzione, la decora (arricchendola con del codice) e la restituisce come valore di ritorno

Serve per alterare (o arricchire) il comportamento di una funzione che esiste già senza modificare direttamente il codice della funzione _(perché per esempio non possiamo farlo)_
```
def myFunc()
	print('la funzione myFunc')

>>>myFunc()
la funzione myFunc
```
>Decoro "a mano" _(senza utilizzare la notazione dei decoratori per adesso)_
```
def myDecorator(f):
	def decorator():
		print('ho decorato')
		f()
	return decorator

def myFunc():
	print('la funzione myFunc')
```
Prendo in input la mia funzione, però in realtà voglio ritornarne come risultato un'altra (decorator)
>La funzione decorator aggiunge una istruzione `print()`;
>Poi invoca la funzione originaria che ha ricevuto come parametro, in questo caso la funzione `f` che poi sarà `myFunc`;
>Ritorna la funzione `decorator`
```
>>>myFunc = myDecorator(myFunc)
>>>myFunc
ho decorato
la funzione myFunc
```

>Mentre con la notazione dei decoratori, scrivo la stessa cosa in questo modo
```
def myDecorator(f):
	def decorator():
		print('ho decorato')
		f()
	return decorator

@myDecorator
def myFunc():
	print('la funzione myFunc')

>>>myFunc()
ho decorato
la funzione myFunc
```
___

#### Funzioni `lambda` _(anonimus function)_
Crea un oggetto funzione _anonimo_, a differenza di `def`
`lambda arg1, arg2, ..., argN : expression (con gli argomenti)`
>Con `def`
```
def myFunc(a, b):
	return a**b
>>>myFunc(2,3)
8
```
>Con `lambda`
```
f = lambda a, b: a**b #funzione anonima che ho chiamato f
>>>f(2,3)
8
```
___
___

# 7. Object-Orientation
_Come si definiscono le nostre classi, come si creano delle istanze a partire da queste classi e poi in generale come si strutturano le classi in gerarchie di generalizzazione_

Python è un linguaggio **Object-Oriented**
>Creare le nostre classi di oggetti, con propri attributi di dati e di codice
>A partire dalle quali si possono creare delle istanze
>Organizzare le classi in gerarchie di generalizzazione, supporto all'ereditarietà
#### Classi ed istanze
2 tipi di oggetti
**Class object**
>Forniscono in generale il comportamento di default, contengono la definizione di una serie di attributi e funzioni che noi stessi andiamo a definire, che servono poi a definire le istanze

**Instance object**
>Oggetti individuali creati (istanziati) dalla definizione delle proprie classi, e che quindi svolgono le attività all'interno dei programmi in python quando noi decidiamo di organizzare questi programmi in modo object-oriented
#### Statement `class`
Statement eseguibile, come lo statement `def` usato per definire le funzioni.
Quando python vede uno statement `class` _(composto da header e suite)_, lo esegue creando l'oggetto **classe**.
```
class classname(base-classes):
	statements
```
>`(base-classes)` _sono una serie di nomi facoltativi di altre classi, le **superclassi**_
>`(class1, class2, class3, ..)`
```
#utilizzo comune è la iniziale maiuscola per il nome delle classi
class MyClass:
	pass
```
>Non avendo messo le parentesi significa che la nostra classe non deriva da altre classi in particolare, ma da quella di default, cioè la classe **object**
```
>>>type(MyClass)
<class 'type'>
#ogni volta che creo una classe, sto creando una istanza della classe type
#la classe type ha come istanze tutte le classi da noi create
```
**Metaclasse**
>`type()` ritorna `type`, che è la **classe base** di _tutte le classi definite dall'utente_.

**Istanze delle nostre classi**
>`myObj = MyClass()` 
>Questa istanza eredita gli _**attributi** che abbiamo definito all'interno della nostra classe_
>Ed ottiene un proprio **namespace**
___








#### Attributi di classe
```
class MyClass:
	myAttr = 10 #attributo della classe

>>> MyClass.myAttr
10

#ora provo a creare 2 istanze dalla stessa classe
>>> m1 = MyClass()
>>> m2 = MyClass()
>>> m1.myAttr
10
>>> m2.myAttr
10

#modifico il valore dell'attributo in una istanza
>>> m1.myAttr = 90 #diventa un suo attributo, dell'istanza m1
>>> m2.Attr
10
>>> MyClass.myAttr
10 #l'attributo di classe non viene modificato
```

>Aggiungere attributi direttamente sulle singole istanze di una classe.
>_sconsigliato_
```
>>> class MyClass():
... 	myAttr = 10
...
>>> m1 = MyClass()
>>> m1.secondAttr = 50
#l'attributo secondAttr appartiene solo all'istanza m1 e non viene in alcun modo condiviso con le altre istanze.
```
___

#### Metodi di istanza
```
class MyClass:
	def myMethod(self):
		print(id(self))
```
_myMethod diventa attributo della classe
`self` è l'istanza su cui chiamo il metodo_
```
>>> m1 = MyClass()
>>> m1.myMethod()
4331160744

>>> m2 = MyClass()
>>> m2.myMethod()
4330225280
```
>Va **sempre** inserito `self` come **primo parametro** nei metodi di istanza
```
class MyClass:
	def myMethod(self, message):
		print(message)

>>> m1 = MyClass()
>>> m1.myMethod('python') #'python' è il message
python
```
___

#### Attributi di istanza
```
class MyClass:
	def setMessage(self, message): #metodo setMessage
		self.message = message
		
#parametro message assegnato ad un attributo di self
#l'attributo `message` che è un dato, non è un attributo di classe, ma è un attributo di ogni singola istanza che viene inizializzato quando chiamo il metodo setMessage passando il messaggio.

	def printMessage(self): #metodo invocato sulle istanze
		print(self.message) #attributo di istanza
```

>Esempio
```
>>> m1 = MyClass()
>>> m1.setMessage('primo')
>>> m2 = MyClass()
>>> m2.setMessage('secondo')
>>> m1.printMessage()
primo
>>> m2.printMessage()
secondo
```
_m1 ed m2 mantengono il proprio valore specifico a livello di istanza per l'attributo message._
**problema**
```
m3 = MyClass()
m3.printMessage()
errore
```
Se creo un'altra istanza e chiamo subito il metodo printMessage, senza aver chiamato prima il metodo setMessage, il programma va in **errore**.
Perché l'attributo non è stato creato all'interno della classe e, di conseguenza, della singola istanza.
Perché non abbiamo chiamato il metodo setMessage.
_Comportamento **debole**!_
>Serve il **costruttore _init_**
___


#### Costruttore `__init__`
Viene sempre invocato automaticamente sull'istanza appena viene creata dalla runtime di python

>**Metodo di istanza**
>Serve a produrre le istanze di una classe.

**Prende sempre `self` come parametro**
>Riprendo l'esempio in _attributi di istanza_:
```
class MyClass:
	def __init__(self, message):
		self.message = message
	def printMessage(self):
		print(self.message)
```

Esempio scorretto
```
>>> m1 = MyClass()
errore
#non ho passato il valore per l'argomento message che __init__ sta aspettando
```

Esempio corretto
```
#passo il valore per l'argomento message per __init__
>>> m1 = MyClass('primo')
>>> m2 = MyClass('secondo')
>>> m1.printMessage()
primo
>>> m2.printMessage()
secondo
```
___



#### Metodi di classe `@classmethod`
Il decoratore `@classmethod` serve per dire a python che questo metodo non è da invocare sulle istanze di una classe, ma sulla classe stessa
```
class MyClass():
	counter = 0 #attributo della classe
	def __init__(self):
		MyClass.counter += 1 #ogni volta che creo una istanza, il counter incrementa di 1
	@classmethod #decoratore
	def istanze(cls): #parametro cls sta per class
		print(cls.counter)

>>> m1 = MyClass()
>>> m2 = MyClass()
>>> m3 = MyClass()
>>> MyClass.istanze()
3
```
_Noto che il parametro **`self` non è presente**, infatti non è un metodo di istanza, ma di classe_.
___

#### Metodi statici `@staticmethod`
**Non acquisisce come primo parametro ne `self` ne `cls`**
>Non si riferisce ne alla classe stessa ne alle istanze
```
class MyClass():
	#staticmethod
	def somma(a,b):
		return(a + b)

>>> s = MyClass.somma(10,5)
>>> print(s)
15
```
___

#### Inheritance _(ereditarietà)_
_Le istanze generate da una classe ereditano gli attributi da quella classe_
Python permette alle classi di ereditare a loro volta degli attributi da altre classi.
>**Superclassi**
>**Sottoclassi**
```
class BClass:
	pass

class AClass(BClass)
	pass

#AClass è sottoclasse di BClass
#BClass è superclasse di AClass
```
___
#### Funzione **isinstance** _(funzione istanza di una classe)_
>_Ritorna un valore booleano_
>Una istanza di una sottoclasse, è istanza anche di tutte le superclassi della sua classe
```
>>> m1 = AClass()
>>> isinstance(m1,AClass)
true
>>> isinstance(m1, BClass)
true
```
___
#### Metodi nella superclasse
```
class BClass:
	def setMessage(self, message):
		self.message = message
	def printMessage(self):
		print(self.message)

class AClass(BClass):
	pass

#sposto questi due metodi in alto nella gerarchia, passando dalla sottoclasse alla superclasse

>>> m1 = AClass()
>>> m1.setMessage('python')
>>> me.printMessage()
python

#l'istanza m1 può usare direttamente i metodi setMessage e printMessage della classe BClass, anche se m1 è una istanza della sottoclasse AClass
```
___
#### Override
**Ridefinire** un attributo definito in una superclasse: _sovrascrittura_
```
class BClass:
	def setMessage(self, message):
		self.message = message
	def printMessage(self):
		print(self.message)

class AClass(BClass):
	def printMessage(self):
		print("AClass " + self.message) #override nella sottoclasse


>>> m1 = AClass()
>>> m1.setMessage('python')
>>> m1.printMessage()
AClass python
```
___
#### Funzione _super_
Accedere ai metodi delle superclassi dall'interno delle sottoclassi.
Se eseguo l'override di un costruttore in una sottoclasse, la superclasse non eseguirà mai più il suo costruttore:
```
class BClass:
	def __init__(self, message):
		self.message = message
	def printMessage(self):
		print(self.message)

class AClass(BClass):
	def __init__(self, valore):
		self.valore = valore
```

>Dato che il costruttore della superclasse non viene **mai** eseguito,
>l'attributo di istanza message della superclasse BClass non verrà **mai** inizializzato.
```
>>> m1 = AClass(20)
>>> m1.valore #metodo sottoclasse
20
>>> m1.printMessage() #metodo superclasse
ERRORE #AClass non ha un attributo message
```
>Uso la funzione **super** per risolvere questo problema
```
class BClass:
	def __init__(self, message):
		self.message = message
	def printMessage(self):
		print(self.message)

class AClass(BClass):
	def __init__(self, valore):
	super().__init__(message)
		self.valore = valore
```
>La funzione super richiamata all'interno di un metodo, in questo caso __int__, ottiene come valore di ritorno la definizione della superclasse.
>Sostituisco alla chiamata alla funzine super l'oggetto classe BClass e su questo invocare il costruttore __init__ passando message come parametro.
>Eseguo il costruttore della superclasse di AClass.

>Il metodo `__init__` di AClass ha **2 attributi**, _message_ e _valore_
>Raccoglie tutti e due gli attributi ed uno lo passa al costruttore della superclasse e l'altro se lo tiene per se ed inizializza il proprio attributo
```
>>> m1 = AClass('python', 20)
>>> m1.valore
20
>>> m1.printMessage()
python
```
Il metodo ora funziona!

_Quando si usa la funzione **super**?_
>In generale, tutte le volte che eseguiamo l'override di un metodo all'interno di una sottoclasse
>Quando però non voglio completamente sovrascrivere il metodo della superclasse, ma voglio **prima eseguire quello della superclasse e poi eseguire il codice del metodo definito in override** all'interno della sottoclasse.

>Quiz
```
class AClass:
	def __init__(self, param):
		self.v1 = param

class BClass(AClass):
	def __init__(self, param):
		self.v2 = param

obj = BClass(100)
print(obj.v1)

ERRORE
```
>Viene generato un **AttributeError** 
>
>Non è stato invocato esplicitamente il metodo `__init__` nella superclasse AClass
>Quindi l'attributo v1 **non è stato creato**
___

#### Properties
**Information hiding**
>Rendono privati gli attributi che presentano dei dati 
>Consentono di accedere agli attributi mediante dei metodi: **setter** e **getter**
>
>Ciò rende **privati gli attributi** e **pubblici i metodi**
```
class MyClass():
	def __init__(self, my_attr):
		self.priv_attr = my_attr

	def get_attr(self):
		return self.priv_attr

	def set_attr(self, attr):
		self.priv_attr = attr

	attr = property(get_attr, set_attr) #coppia di attributi che sono funzioni (metodi)
```
>Accesso alla property
```
>>> obj = MyClass('python')
>>> obj.attr
'python'
>>>obj.attr = 'prova'
>>>obj.attr
'prova'
```
>Accesso **diretto** alla property
```
>>> obj.set_attr('python')
>>> obj.get_attr()
'python'
>>> obj.priv_attr = 'prova'
```
>**Nascondere** un attributo `__`
```
class MyClass():
	def __init__(self, my_attr):
		self.__priv_attr = my_attr

	def get_attr(self):
		return self.__priv_attr

	def set_attr(self, attr):
		self.__priv_attr = attr

	attr = property(get_attr, set_attr)

>>> obj = MyClass('python')
>>> obj.__priv_attr
Traceback (most recent call last):
	File "<stdin>", line 1, in <module>
AttributeError: 'MyClass' object has no attribute '__priv_attr'
```
Come nasconde l'attributo?
>**Name mangling**
```
>>> obj._MyClass__priv_attr
'python'
```
Aggiunge un underscore `_` all'inizio, quindi viene salvato diversamente.
___




#### Property decoration
Posso utilizzare **2 decoratori**:

>**`@property`** _decoratore del metodo **getter**_

>**`@name.setter`** _decoratore del metodo **setter**_

```
class MyClass():
	def __init__(self, my_attr):
		self.__priv_attr = my_attr

	@property
	def attr(self):
		return self.__priv_attr

	#attr.setter
	def attr(self, my_attr):
		self.__priv_attr = my_attr


>>> obj = MyClass('python')
>>> obj.attr
'python'
>>> obj.attr = 'test'
>>> obj.attr
'test'
```
____
