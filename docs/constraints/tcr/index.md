---
tags:
- constraint
---

# Test && Commit || Revert

> Outillage : <br>
> 🔗 https://github.com/murex/TCR <br>
> 🔗 https://github.com/murex/TCR/blob/main/examples

À chaque fois que le code est modifié et sauvegardé, les tests sont lancés.

- Si tous les tests passent, le code est commité
- Si au moins un test échoue, le code de prod est revert