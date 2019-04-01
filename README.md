# LaTeKiSS

**LaTeKiSS** è un template *[pandoc][]* per tesi di laurea. Il suo obbiettivo è sollevare gli studenti dall'impaginazione, in modo da concentrarsi esclusivamente sul contenuto della tesi.

*LaTeKiSS* è realizzato in modo da essere quanto più possibile *LaTex-free* per l'utente finale. 
Lo studente, così, potrà scrivere la sua tesi in *markdown* e inserire le informazioni extra tramite un file `.yaml`.
Nella seguente guida è specificato come adattare il template alle proprie necessità e come ottenere il documento finale.

Questo template usa il pacchetto LaTeX [ClassicThesis][classicthesis] realizzato da André Miede.

---

## Guida

### Installazione

- Installare pandoc e una distribuzione LaTeX.
- Scaricare l'ultima versione di questo tema dalla pagina delle release.
- Copiare il file `latekiss.tex` nella cartella dei template e rinominarlo in `latekiss.latex`. La cartella dei template varia a seconda del sistema operativo.
  - Unix, Linux, macOS: `~/.pandoc/templates/`
  - Windows XP: `C:\Documents And Settings\USERNAME\Application Data\pandoc\templates`
  - Windows Vista o superiore: `C:\Users\USERNAME\AppData\Roaming\pandoc\templates`

### Utilizzo

Una volta installato tutto il materiale necessario sarà specificare l'utilizzo del tema *LaTeKiSS* durante la compilazione tramite pandoc.
Per esempio nel caso in cui l'intera tesi sia stata scritta all'interno del file `thesis.md` e i vari metadati più tutte le impostazioni per la compilazione siano contenute nel file `metadata.yaml` è possibile ottenere il documento formattato in pdf attraverso il seguente comando.

Nella cartella `samples` sono disponibili alcuni esempi di utilizzo.

```bash
pandoc thesis.md metadata.yaml -o thesis.pdf --template latekiss
```

### Variabili

- `abstract` (string)
  abstract del documento
- `abstract-title` (string)
  titolo della pagina dell'abstract
- `academic-year` (string)
  anno accademico
- `acronym` (lista)
  - `name`(string)
  nome dell'acronimo
  - `description` (string)
  descrizione dell'acronimo
- `acronym-title` (string)
  titolo della pagina degli acronimi
- `acknowledgments `(string)
  ringraziamenti
- `acknowledgments-title `(string)
  titolo della pagina dei ringraziamenti
- `author` (string)
  nome e cognome dell'autore
- `babel` (string)
  lingua del pacchetto babel
- `bibliography `(string)
  path del file .bib
- `copyright` (string)
  messaggio di copyright
- `course` (string)
  il corso di laurea che si sta frequentando
- `dedication `(string)
  dedica
- `dedication-title` (string)
  titolo della pagina di dedica
- `department` (string)
  il dipartimento a quale afferisce il corso di laurea
- `draf` (string)
  versione della bozza. Da non specificare nel documento finale
- `eulerchapternumber` (boolean)
  usa il font AMS Euler per il numero del capitolo. Palatino come font di default
- `floatnumbering` (boolean)
  usa la numerazione float per le figure e le altre risorse. False come valore di default
- `fontsize `(string)
  grandezza del carattere. 11pt come valore di default
- `hidelinks `(boolean)
  se impostato i link appaiono in nero. Falso come valore di default
- `institute `(string)
  l'istituto al quale si è iscritti
- `keywords` (lista di string)
  lista con le parole chiave del documento
- `lineheaders` (boolean)
  aggiunge una linea di separazione tra il numero del capitolo e il nome del capitolo. Falso come valore di default
- `logo` (string)
  path del logo dell'università
- `matr` (int)
  matricola dell'autore
- `monochrome` (boolean)
  se impostato gli snippet saranno in bianco e nero. Falso come valore di default
- `onlyused` (boolean)
  stampa solo gli acronimi utilizzati nel testo. Falso come valore di default
- `openright` (boolean)
  il capitolo inizia sempre alla pagina destra. Falso come valore di default
- `paper` (string)
  grandezza del foglio. A4 come valore di default
- `quote` (string)
  citazione
- `quote-author` (string)
  autore della citazione
- `subject` (string)
  oggetto della tesi
- `subtitle `(string)
  sottotitolo della tesi
- `supervisor`
  - `name` (string)
    nome del relatore
  - `title` (string)
    titolo del relatore
- `style` (string)
  consente di impostare lo liste della tesi tra classicthesis e arsclassica. classicthesis come valore di default
- `title` (string)
  titolo della tesi
- `toc` (boolean)
  include l'indice
- `toc-aligned` (boolean)
  allinea l'indice. False come valore di default
- `toc-depth` (int)
  configura la profondità dell'indice. Due come valore di default
- `toc-dotted` (boolean)
  allinea i numeri di pagina a destra aggiungendo i puntini. False come valore di default
- `toc-title` (string)
  configura il titolo dell'indice
- `lof` (boolean)
  include l'indice delle figure
- `lof-title` (string)
  configura il titolo dell'indice delle figure
- `lot` (boolean)
  include l'indice delle tabelle
- `lot-title` (string)
  configura il titolo dell'indice delle figure
- `twoside` (boolean)
  se si desidera ottenere pagina destra e pagina sinistra. Falso come valore di default

[pandoc]: https://pandoc.org/

[classicthesis]: https://bitbucket.org/amiede/classicthesis/wiki/Home
