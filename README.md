# workshop-commons

Questa directory contiene risorse riutilizzabili per costruire presentazioni di workshop con Slidev.

## Risorse

### Temi

  * **modern-minimal**: Un tema scuro moderno, minimale e professionale.

### Stili

  * **overrides.css**: Utilità CSS opzionali e componenti (card, griglie, badge, box informativi, ecc.)

### Template di Slide

  * **intro/montelli-intro.md**: Una slide di introduzione standard per i workshop di Francesco Montelli.

## Come Usare

Per usare queste risorse nella tua presentazione Slidev, fai riferimento ad esse usando percorsi relativi dal tuo file markdown principale.

### Usare il Tema

Nel frontmatter del tuo file `slides.md` (o simile), imposta la proprietà `theme`.

**Esempio (dalla root del progetto):**

```yaml
---
theme: './workshop-commons/themes/modern-minimal'
---
```

**Esempio (da una sottocartella `slides`):**

```yaml
---
theme: '../workshop-commons/themes/modern-minimal'
---
```

### Usare gli Stili CSS (Overrides)

Per usare le utilità CSS opzionali, importale nel frontmatter della tua presentazione o in un tag `<style>`.

**Esempio (in frontmatter):**

```yaml
---
theme: '../workshop-commons/themes/modern-minimal'
---

<style src="../workshop-commons/styles/overrides.css"></style>
```

#### Utilità Disponibili & Esempi

Ecco una guida alle classi più comuni in `overrides.css` e come usarle all'interno delle tue slide.

-----

**Griglie (`.grid-cols-2`, `.grid-cols-3`)**

Creano un layout a 2 o 3 colonne per organizzare il contenuto.

```html
<div class="grid-cols-2">

<div>
**Colonna 1**
Contenuto della prima colonna.
</div>

<div>
**Colonna 2**
Contenuto della seconda colonna.
</div>

</div>
```

-----

**Card (`.card`)**

Applica uno stile "card" a un blocco di contenuto, con padding, bordi e un leggero effetto hover.

```html
<div class="card">
<h3>Titolo della Card</h3>
<p>Questo è il contenuto all'interno della card. È utile per raggruppare visivamente le idee.</p>
</div>
```

-----

**Box Informativi (`.info-box`, `.warning-box`)**

Blocchi di avviso colorati per evidenziare note importanti o attenzioni.

```html
<div class="info-box">
💡 **Nota:** Ricorda di eseguire `npm install` prima di iniziare.
</div>

<div class="warning-box">
⚠️ **Attenzione:** Modificare questo file potrebbe rompere la configurazione.
</div>
```

-----

**Dimensioni Emoji (`.emoji-small`, `.emoji-medium`, `.emoji-large`)**

Classi veloci per ridimensionare gli emoji, utili per slide di sezione o Q\&A.

```html
<div class="emoji-large">
🎤
</div>

<h3>Q&A</h3>

<p>Testo normale con un emoji <span class="emoji-small">✅</span></p>
```

-----

**Badge (`.badge`)**

Crea una piccola etichetta (badge) colorata, utile per tag o per evidenziare uno stato.

```html
<h3>Nuova Feature <span class="badge">BETA</span></h3>
```

-----

**Testo Evidenziato (`.highlight`)**

Evidenzia un frammento di testo con il colore primario del tema.

```html
<p>
È <span class="highlight">fondamentale</span> capire questo concetto
per proseguire con il workshop.
</p>
```

-----

*(e altre utilità...)*

### Usare i Template di Slide

Puoi includere template di slide esterni usando la proprietà `src` su un separatore di slide.

**Esempio (dalla root del progetto):**

```markdown
---
src: ./workshop-commons/slides/intro/montelli-intro.md
---
```