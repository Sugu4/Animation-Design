# WebMiete24 Hero Scroll Animation

Ein minimalistischer Hero-Bereich mit Parallax-Scroll-Effekt und animiertem WebMiete24‑Logo (SVG). Beim Scrollen bleibt der Hero kurz „gepinnt“, das Hintergrundbild bewegt sich langsamer als der Inhalt, und das Logo reagiert auf Hover mit einer leichten Motion.[web:74][web:77][web:191]

## Features

- Parallax-Hintergrundbild mit Scroll-basiertem Zoom & Translate.[web:187][web:191]  
- Gepinnter Hero-Bereich (`position: sticky`), der erst nach definierter Scrollstrecke freigibt.[web:93]  
- Inline-SVG-Logo *WebMiete24* oben links, mit Hover-Animation (Translate/Scale).[web:40]  
- Einfache Responsive-Anpassung via `@media (max-width: 768px)` für Mobile.[web:86]  

## Struktur

- **index.html**  
  - `hero-wrapper`: Container, der die Scroll-Dauer des Heros steuert.  
  - `hero`: sticky Hero-Section (100vh) mit Hintergrundbild (`hero-bg`) und Inhalt (`hero-content`).  
  - `hero-logo`: absolut positioniertes WebMiete24‑Logo (SVG) oben links.  
  - Mehrere `section`‑Blöcke als Demo-Content unter dem Hero.

## Nutzung

1. Projekt-Datei (z. B. `index.html`) in einen Ordner legen.  
2. Hintergrundbild-Pfad im CSS anpassen:
.hero-bg {
background: url(assets/bild/pexels-gdtography-277628-911738.jpg) center/cover;
}
3. `index.html` im Browser öffnen.  
4. Scrollen, um den Parallax-Effekt zu sehen; mit der Maus über das Logo hovern, um die Logo-Animation zu triggern.

## Anpassung

- **Scroll-Dauer des Heros**: in `.hero-wrapper` `height: 220vh;` erhöhen oder verringern.  
- **Parallax-Intensität**: im Script `rate = progress * -80;` und `scale = 1.1 + progress * 0.2;` anpassen.  
- **Logo-Animation**: CSS-Selektoren `.wm24-logo`, `.wm24-icon`, `.wm24-24` modifizieren (z. B. andere `transform`‑Werte oder `transition`‑Dauer).[web:40][web:75]  

## Tech Stack

- **HTML5** für Markup.  
- **CSS3** (Flexbox, Media Queries, Transforms, Transitions) für Layout & Animation.  
- **Vanilla JavaScript** für die Scroll-basierte Parallax-Berechnung ohne externe Libraries.[web:191][web:197]

