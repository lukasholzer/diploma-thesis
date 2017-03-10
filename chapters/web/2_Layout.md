# Das Layout

## Erklärungen

### Media Queries
Media Querys sind Abfragen, die es dem Medium *(in diesem Fall dem Browser)* ermöglichen zu ermitteln welche Breite der sogenannte **view-port** *(Innere Bereich eines Browserfensters)* hat. Anhand dieser Media queries werden dann Syleregeln angewendet. Eine Media Query verfügt auch über die Optionalität die Ausrichtung eines Geräts, wie Hochformat oder Querformat, oder auch die Pixeldichte *(für Retinageräte)* abzufragen.
### Breakpoints
Breakpoints sind bestimmte Punkte oder Punktespannen, gemessen in px, welche bestimmte Bereiche definieren. Diese Bereiche werden dann auf die Media Queries angewandt, um eine bestimmte Layoutregel darauf anzuwenden.
Die folgenden Breakpoints wurden bei der Website verwendet um die folgenden 5 Gerätegrößen abzudecken.

| von px | bis px | Gerät             |
| ------ | ------ | ----------------- |
| 0      | 510    | Mobile Devices    |
| 511    | 768    | Tablets           |
| 769    | 1200   | Laptops           |
| 1201   | 1440   | Desktops          |
| 1441   | ∞      | Ultra Wide        |


## wie alles anfing
(Fixed Layouts und der Beginn des Webs)

## Responsive Layouts

## Fluid oder liquid layouts
Der Begriff fluid oder liquid Layout kommt davon, dass dieses ohne fixen Breitenangaben auskommt. Das heißt alles wird in Prozent gerechnet und behält dadurch seine Proportionen bei Skalierung des Browserfensters. Das klassische Beispiel für ein Liquid Layout wäre die Einteilung von Sidebar und Main Bereich, wo der Hauptteil eine Breite von 70% hat und die Sidebar eine Breite von 30%. 
Diese Technik kommt jedoch oft mit der Kombination von Media Queries vor, da diese ermöglicht andere Prozentuale Verhältnisse für mobile Geräte zu definieren. Im Beispiel der Sidebar würde das bedeuten, dass diese auf mobilen Geräten eine Breite von 100% erreichen würde und sich unter den Hauptteil fügen würde. Dieses flüssige behalten ist der Hauptgedanke eines Fluid Layouts. Es beschreibt den Fluss der Elemente auf verschiedenen Endgeräten. Dieses Phänomen kann man nicht nur beim Vergrößern des Browserfensters begutachten, sondern auch beim Ändern der Geräteausrichtung, von Horizontal auf Vertikal oder vice versa.
> vgl. Implementing Responsive Design p.25


## Elastic Layouts

## Hybrid Layouts
Die letzte und Layoutoption ist das Hybride Layout. Es kombiniert die Eigenschaften der vorangehenden Beispiele.
Dies Kommt zum Beispiel bei unserem Grid Layout vor. Da der Abstand der Grid Spalten, die *grid-gap* in px angegeben ist. Dadurch dass ein sogenanntes 12er grid (bestehend aus 12 Spalten) im Einsatz ist passt sich die Breite einer einzelnen Spalte dem restlichen Platz an. Zusätlich steuern noch Media Queries mit einem Breakpoint für mobile Endgeräte die *grid-gap*, damit diese auf Smartphones zum Beispiel geringer ist.


The last Layoutoption is the hybrid layout. It combines the abilitys of the previous examples.
