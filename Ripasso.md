# HTML5 - ripasso

## 1 - Markup: Linguaggio di programmazione? nope!

Linguaggio di programmazione -> da istruzioni su cosa fare

Linguaggio di markup -> fa due cose:

dice cosa rappresentare e come rappresentarlo nella pagina! (contenuto e istruzioni all'uso)

https://guides.github.com/features/mastering-markdown/

I file .md che github renderizza sono file che utilizzano un liguaggio di markup! 

Io sono un file scritto in un linguaggio di markup chiamato markdown! (infanzia difficile...

### Tags

L'elemento principale di questi linguaggi e' il tag, una specie di segnaposto per dire che quelle sono le istruzioni di rappresentazione e non il contenuto

 - < sono un tag aperto > contenuto </ sono lo stesso tag chiuso >
 - /# <- anche quello e' un tag (in mardown)

in html e' meglio che itag siano minuscoli, ma in teoria e' case insesitve

## 2 - HTML5 caratteristiche

HTML è un linguaggio di markup che permette di definire documenti testuali che il browser interpreta come istruzioni per predisporre gli elementi di una pagina web.

Piu' genericamente e' un linguaggio usato per specificare la disposizione degli elementi di una interfaccia, a patto che ci sia un "interprete che poi sappia renderizzarlo.

Sono file di testo con estensione **.html**, provate a giocarci qui:

https://www.w3schools.com/tryit/tryit.asp?filename=tryhtml_hello

## 3 - Anatomia di una pagina HTML

Quando carichiamo una pagina web, il browser crea in memoria un oggetto che rappresenta l'albero della struttura, come vediamo qui sotto, dove sono definiti gli elementi in maniera gerarchica e le proprieta'. Questo oggetto e' chiamato DOM, per ora teniamolo a mente lo rincontreremo...

per i piu' curiosi -> https://www.w3schools.com/whatis/whatis_htmldom.asp

Intanto cominciamo a vedere un dom minimale e capiamo come sono fatti gli elementi.

>&lt;!DOCTYPE html>
  &lt;html>
  &lt;head> *metadati* &lt;/head>
  &lt;body> *contenuto* &lt;/body>
  &lt;/html>

https://www.w3schools.com/html/html_basic.asp

### 3.1 - &lt;head>

---

https://www.w3schools.com/html/html_head.asp
contiene tipicamente metadati, vediamo quelli piu' importanti (date un occhiata alla pagina qui sopra):

#### Title 
>&lt;title>&lt;/title>
>
https://www.w3schools.com/html/html_head.asp
titolo della pagine e appare nella toolbar

### link
per inserire fogli di stile (css), file di script (javascript) necessari alla renderizzazione coretta dal punto di vista della resa grafica e del funzionamento:

> &lt;link rel="stylesheet"  href="CSS/style.css"> 


### viewport 

il viewport e' un concetto del mondo interfacce per rappresentare la porzione di schermo in cui potete inserire elementi e che il browser renderizza (rappresnta lo schermo utile)

> &lt;meta name="viewport"  content="width=device-width, initial-scale=1.0">

buona norma mettere questo cosi' da dare alla pagina un minimo di "responsivenness"

### 3.2 &lt;body>
---
Compreso in questo tag mettete tutto il contenuto della pagina che deve essere mostrato.
Praticamente tuttti i tag, a parte quelli sopracitati per head, sono da inserire qui

#### contenitori generici

vi permettono di raggruppare altri oggetti per creare un elemento composito nella vostra pagina.

Vedrete quanto sono fondamentali, ma guardateli con attenzione da soli...

https://cs.wellesley.edu/~cs110/reading/div-span-id-class.html

#### &lt;h> headings
titoli e sottotitoli a partire da 
> &lt;h1>&lt;/h1> 
> ... 
> &lt;h6>&lt;/h6>
#### &lt;p> paragrafi
paragrafo per iserire del testo normale.

> &lt;p>&lt;/p>

allineamneto del testo... e non solo

>&lt;p align=”center”>&lt;/p>
>&lt;p align=”left”>&lt;/p>
>&lt;p align=”right”>&lt;/p>
>&lt;p align=”justify”>&lt;/p>

#### modificatori del testo 
**grassetto**  
> &lt;b>&lt;/b>
> 
*italico* 
> &lt;i>&lt;/i>
#### links

Permette di passare da una pagina all'altra, di andare alla risorsa puntata dal link

Gli URL possono essere di due tipi: un percorso su file system oppure un indirizzo http tradizioanale.

>&lt;a href=”URL”>testo del link&lt;/a>

#### liste

- unorderd list 
- (bullet list) 
- lista disordinata

> &lt;ul> 
> &lt;li>elemento lista&lt;/li>
> &lt;li>altro elemento&lt;/li>
> &lt;/ul>

---

 1. lista ordinata
 2. numerata
 3. in ordine

> &lt;ol> 
> &lt;li>elemento lista&lt;/li>
> &lt;li>altro elemento&lt;/li>
> &lt;/ol>

#### forms

i form sono una delle funzionalita' piu' usate dell'html, in quanto permettono di ricevere informazioni dall'utente.

>&lt;form action=”...” method=”...” name=”...”> &lt;/form>

 - action  -> di solito uno scipt che si occupa di gestire il comportamento associato all'azione
 - method -> GET e POST del protocollo http
 - name -> nome univoco affinche' sia riconoscibile dal server/script

vi rimando qui per le info: https://www.w3schools.com/html/html_forms.asp

![enter image description here](https://1.bp.blogspot.com/-4XVpHqLWDSg/X4PUs7P6dWI/AAAAAAAAjyk/sWQQJ4ztHtQUs8GhDnmOdjSecNuqT9EpwCLcBGAsYHQ/w1200-h630-p-k-no-nu/difference_between_get_and_post_method_http.png)

![enter image description here](https://miro.medium.com/max/1400/0*wGBQskLJo5AB98hS)

![enter image description here](https://slideplayer.com/slide/15650516/88/images/7/GET+vs.+POST+scenarios+Browser/JS+sends+HTTP+GET+request+with+parameters.+Fill+out+form+and+press+SEND..jpg)

#### input type

nei form e' possibile specificare dei particolari tipi di campi per i form, ad esempio:

> &lt;input type=”password” name="loginpass">

crea un campo in cui sara' possibile inserire password (cioe' che nascondera' ad esempio a schermo i caratteri digitati)

E' inoltre possibile passare un valore all'elemento quando non e' necessario che l'utente mandi nulla ma sia una selezione:

> &lt;input type=”checkbox” name ="terms_acepted" value="privacy_terms">


e' molto importante da uno sguardo a queste pagine, perche' coprirli tutti ci vorrebbero ore..

https://www.w3schools.com/html/html_form_elements.asp

https://www.w3schools.com/html/html_form_input_types.asp



#### immagini e altri media

Fate riferimento ai formati compatibili di media qui:

https://www.w3schools.com/html/html_media.asp

Intanto prendiamo ad esempio le immagini:

> &lt;img src="_url immagine_"  alt="_alternatetext_">

Il testo alternativo appare se non si riesce a caricare l'immagine, e viene letto quando, ad esempio, un non vedente naviga con una estesione particolare.

Per maggiori informazioni vi rimando alla pagina dedicata:

https://www.w3schools.com/html/html_images.asp

per gli altri media:

 - https://www.w3schools.com/html/html5_audio.asp
 - https://www.w3schools.com/html/html5_video.asp
 - https://www.w3schools.com/html/html_youtube.asp
 - https://www.w3schools.com/html/html_object.asp
