# Kredithjørnet — nyt design (fælles stylesheet)

Statisk website (ren HTML + ét fælles CSS-ark) til GitHub Pages med domænet kredithjornet.dk.
Intet byggeværktøj, ingen afhængigheder.

## Sådan virker det
- Hver side er en almindelig .html-fil.
- ALT design ligger i én fil: `css/style.css`. Hver side linker til den med:
  `<link rel="stylesheet" href="/css/style.css">`
- Vil du ændre designet, retter du i `css/style.css` ét sted — så slår det igennem på alle sider.
- Pæne URL'er laves med mapper: en mappe + en index.html giver fx /boliglaan-selvstaendig/

## Hvad mappen indeholder lige nu
- `index.html` .................................. Forside (design source of truth)
- `boliglaan-selvstaendig/index.html` .......... Pillar: Boliglån som selvstændig
- `css/style.css` .............................. Fælles designark for HELE sitet
- `favicon.svg` ................................ Faneikon (grønt hus-mærke)
- `CNAME` ...................................... Custom domain (kredithjornet.dk)

Resten af Sprint 1-siderne (freelancer, dokumentation, nyt firma, bankskifte,
omlægning, beregner, om, kontakt, privatlivspolitik m.fl.) leveres i de næste
opdateringer og lægges i samme mappe, alle med link til samme `css/style.css`.

## Sådan lægger du det i GitHub (når hele sættet er klar)
Dette er en KOMPLET udskiftning til det nye design. Vent med at committe,
til alle Sprint 1-siderne er leveret. Gør så følgende i GitHub Desktop:

1. Slet alt det gamle i repo-mappen på din computer (de gamle sider i det
   tidligere design). Mappen skal være tom.
2. Kopier HELE indholdet af denne mappe ind (index.html, css/, alle undermapper,
   favicon.svg, CNAME).
3. I GitHub Desktop: skriv en kort linje i "Summary" (fx: Nyt design – komplet site)
   og klik "Commit to main", derefter "Push origin".

Indtil du committer, ligger dit nuværende site stadig urørt på github.com.

## GitHub Pages + domæne
- Settings → Pages → Source: "Deploy from a branch" → main / root.
- Settings → Pages → Custom domain: kredithjornet.dk (CNAME-filen sikrer den binding).
- DNS hos simply.com peger allerede på GitHub Pages — det skal ikke ændres.

## Vigtigt: Mybanker-knappen
Den primære "Sammenlign"-CTA peger på `href="#"`, indtil Mybanker-programmet er
godkendt i Adtraction. Søg i HTML-filerne efter kommentaren
"Erstat href med Adtraction-trackinglink" og indsæt det rigtige link, når det er klart.
