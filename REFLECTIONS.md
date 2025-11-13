Hvad er fordelene ved global CSS?
Global CSS er simpelt at sætte op og godt til styles, der gælder hele appen: resets, skrifttyper, layout-variabler og utility-klasser. Det loader én gang (typisk i `globals.css`), hvilket gør det praktisk til overordnede temaer og base-styling. Ulempen er risiko for navnekonflikter og utilsigtet påvirkning af komponenter.

Hvad er fordelene ved CSS Modules?
CSS Modules giver lokal scope for class-navne, så stilregler kun påvirker den komponent, de hører til. Det gør refaktorering tryggere, undgår kollisionsproblemer og holder komponenter kapslet. Modules spiller godt sammen med komponentdrevet udvikling.

Hvornår ville du bruge det ene frem for det andet?
Brug global CSS til app-omfattende ting: resets, fonts, CSS-variabler, globale helper/utility-klasser og layout. Brug CSS Modules til komponent-specifik styling, når du vil undgå sideeffekter og gøre komponenter genanvendelige. I Next.js er en god praksis: `globals.css` til base + `Component.module.css` ved komponenter.

Hvordan undgår projektet CSS konflikter?
Projektet undgår konflikter ved at bruge CSS Modules til komponenter (automatisk scoping) og ved at holde global CSS minimal og veldefineret. Yderligere strategier er konsekvente navngivningskonventioner, begrænset brug af globale klassenavne, og eventuelt værktøjer som Tailwind eller CSS-in-JS når isolation er vigtig.

Hvad er fordelen ved at bruge CSS variabler?
CSS-variabler øger genbrugeligheden og gør temaer og justeringer nemme — værdier kan ændres centralt eller per scope (f.eks. for dark mode). De kan ændres ved runtime (gør dynamisk tema-ændring enkel) og kombineres med JavaScript når nødvendigt.
