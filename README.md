# Passrotation

Enkel gymtracker: håller koll på vilket av sex pass som är nästa i rotationen
(Ben & Rygg, Axel & Bröst, Biceps & Triceps – två varianter var, byggda kring
hantlar och träningsbänk), och visar statistik över genomförda pass.

**Använd appen här:** https://claude.ai/code/artifact/e7cf54dc-0c52-4474-99fd-f0b813a4b603

Detta repo är källkoden (`index.html`), versionerad för historik. Själva
appen körs som en Claude Artifact eftersom den använder Artifacts inbyggda
molndatabas för att synka loggen mellan enheter, utan egen backend.

## Rotation

1. Ben & Rygg (A)
2. Axel & Bröst (A)
3. Biceps & Triceps (A)
4. Ben & Rygg (B)
5. Axel & Bröst (B)
6. Biceps & Triceps (B)

Nästa pass räknas ut från senast genomförda pass i loggen – ingen manuell
inställning behövs.
