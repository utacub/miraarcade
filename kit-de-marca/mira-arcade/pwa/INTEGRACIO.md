# Integració dels recursos PWA de Mira Arcade

## Aplicació dels fitxers

La carpeta `icons/` conté els PNG i el favicon. El manifest utilitza rutes relatives i està preparat per situar-se a l’arrel de l’app publicada a `/miraarcade/`.

1. Copia el contingut de `icons/` a la carpeta `icons/` del projecte.
2. Revisa i incorpora `manifest.webmanifest`. Conserva `id`, `start_url` i `scope` amb el valor `./`, així com el blau nit `#090B14` de la configuració consultada.
3. Integra les etiquetes de `head-snippet.html` al document HTML, revisant les que ja hi hagi per evitar duplicacions.
4. Utilitza el logotip principal amb lletres blanques al capçal o a la pantalla inicial sobre fons fosc.
5. Si el projecte precarrega icones al service worker, incorpora les noves rutes al mecanisme de memòria cau.
6. Després de publicar, comprova el manifest i les icones al navegador i prova la instal·lació en els sistemes objectiu. La validació d’aquest paquet comprova fitxers i geometria; no substitueix la prova en dispositius.

## Icones normals i adaptables

Els fitxers `icon-192.png`, `icon-512.png` i `icon-1024.png` són les icones normals. Els `icon-maskable-*.png` tenen més marge. El manifest en diferencia les finalitats amb `purpose: any` i `purpose: maskable` (MDN contributors, 2025).

Les icones tenen fons opac. A les versions maskable s’ha comprovat que el símbol essencial queda dins el cercle protegit central de radi 40% (MDN contributors, 2025; Steiner & Oakes, s. d.).

## iPad i iPhone

S’inclouen Apple Touch Icons de 152, 167 i 180 px i l’àlies `apple-touch-icon.png` de 180 px. Les etiquetes amb `sizes` permeten indicar les diverses resolucions, d’acord amb la documentació d’Apple (Apple, s. d.).

## Referències

Apple. (s. d.). *Configuring web applications*. Safari Web Content Guide. https://developer.apple.com/library/archive/documentation/AppleApplications/Reference/SafariWebContent/ConfiguringWebApplications/ConfiguringWebApplications.html

MDN contributors. (2025, 30 de juny). *Define your app icons*. MDN Web Docs. https://developer.mozilla.org/en-US/docs/Web/Progressive_web_apps/How_to/Define_app_icons

Steiner, T., & Oakes, T. (s. d.). *Adaptive icon support in PWAs with maskable icons*. web.dev. https://web.dev/articles/maskable-icon
