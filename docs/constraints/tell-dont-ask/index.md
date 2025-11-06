---
title: 👑 Tell, don't ask
tags:
  - constraint
  - constraint/code
---

# 👑 Tell, don't ask

> 🔗 https://martinfowler.com/bliki/TellDontAsk.html

Il est interdit d'interroger les objets sur leur état interne pour prendre des décisions à leur place.
Vous ne pouvez pas récupérer la donnée de vos objets pour la manipuler ensuite, par exemple dans des calculs externes.

À la place, vous devez déléguer à vos objets la responsabilité d'effectuer les opérations via des méthodes comportementales. 

!!! experiment "Exemple"

    🚫 Evitez
    ```
    if (obj.getStatus() == "ready") {
     obj.setValue(x);
    }
    ```
    ✅ Privilégiez
    ```
    obj.activate(x)
    ```

Les getters purs servant uniquement à l'affichage final ou aux assertions de tests restent autorisés, mais tout traitement métier doit être encapsulé dans l'objet concerné.