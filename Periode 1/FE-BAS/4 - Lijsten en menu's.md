

In HTML kun je lijsten maken. Vaak zie je bij frontend opdrachten dat er **ordered lists (ol)** en **unordered lists (ul)** worden gebruikt. Een lijst-element omsluit altijd de hele lijst en bevat **list items (li)**.

**Waar worden list elements voor gebruikt?**

- **Unordered list (ul):** lijst zonder volgorde, bijvoorbeeld ingrediënten van een gerecht.
    
- **Ordered list (ol):** lijst met volgorde, bijvoorbeeld stappen bij een recept of instructies.
    

**Tip:** Stappen → **ordered list**, Instructies per stap → **unordered list**

**Structuur van een lijst:**

- De hele lijst staat in een `<ol>` of `<ul>`.
    
- Lijsten kunnen **sublijsten** bevatten, en dat kan **oneindig** diep.
    
- Sublijst maak je door een nieuwe lijst binnen een `<li>` te openen.
    

**Voorbeeld HTML:**

```html
<ol>
  <li>
    Dit is het eerste item.
    <ul>
      <li>Subitem 1</li>
      <li>Subitem 2</li>
      <li>Subitem 3</li>
    </ul>
  </li>
  <li>
    Dit is het tweede item.
    <ul>
      <li>Subitem 1</li>
      <li>Subitem 2</li>
      <li>Subitem 3</li>
    </ul>
  </li>
</ol>
```

**Waarom zijn lijsten perfect voor navigatiemenu's?**

- Websites hebben een **hiërarchische structuur**: 1 hoofdpagina bovenaan en onderliggende pagina's daaronder.
    
- Navigatiemenu's gebruiken vaak **lijsten** om deze structuur duidelijk te maken.
    
- Hierdoor kan een gebruiker makkelijk navigeren zonder HTML/JS kennis.
    

**Samengevat:**

- **UL** → geen volgorde nodig
    
- **OL** → volgorde belangrijk
    
- **LI** → elk item in de lijst
    
- **Sublijsten** → voor hiërarchie of nested content
    
- **Navigatiemenu** → gebruik lijsten voor overzicht en structuur