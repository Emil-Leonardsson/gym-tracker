# Passrotation

Enkel gymtracker: håller koll på vilket av sex pass som är nästa i rotationen
(Ben, Rygg & Mage / Axel, Bröst & Mage / Biceps, Triceps & Mage – två
varianter var, byggda kring hantlar, träningsbänk och sittup-bänk), loggar
när varje pass startas och avslutas, och visar statistik över genomförda
pass.

**Använd appen här:** https://emil-leonardsson.github.io/gym-tracker/

Kräver inloggning (magic link via e-post) – ingen träningsdata visas eller
går att nå förrän du är inloggad.

Detta repo är källkoden (`index.html`), en helt statisk sida utan
byggsteg, hostad direkt via GitHub Pages. Den pratar med en Supabase-databas
(delad med Emils andra små personliga appar, se
[Emil-Leonardsson/shared-db](https://github.com/Emil-Leonardsson/shared-db)
för schema/migrationer) via `@supabase/supabase-js`, med Supabase Auth
(magic link) och rad-nivå-behörigheter som begränsar varje inloggad
användare till sina egna rader.

Körde tidigare som en Claude Artifact med Artifacts inbyggda molndatabas;
flyttades 2026-09-15 till GitHub Pages + Supabase för en publik URL utan
claude.ai-inloggning.

## Rotation

1. Ben, Rygg & Mage (A)
2. Axel, Bröst & Mage (A)
3. Biceps, Triceps & Mage (A)
4. Ben, Rygg & Mage (B)
5. Axel, Bröst & Mage (B)
6. Biceps, Triceps & Mage (B)

Nästa pass räknas ut från senast genomförda pass i loggen – ingen manuell
inställning behövs. Efter sju pass (ett helt varv, med det första passet
upprepat som referens) firas ett extra "superstämpel"-ögonblick och raden
återställs för nästa varv, utan att statistiken nollställs.
