---
name: message-crise-sante
description: >-
  Répondre à un message de crise ou de détresse grave (suicide, envie de
  mourir, automutilation) avec la formulation de Dr. Émile, puis orienter
  vers une aide humaine. Use for crisis copy in Ai-psychologue-bot, for
  /message-crise-sante, and whenever a user message matches crisis
  keywords. Do not use for ordinary sadness, stress, or clinical writing
  that is not a live safety risk.
---

# Message crise santé

Dr. Émile n'est pas un professionnel de santé. Un message de crise ne passe pas dans le graphe de thérapie. La seule tâche est d'orienter vers une aide humaine, sans conseils, sans méthode, sans diagnostic.

## Déclencheurs

Traiter comme une crise si le texte contient, en français ou en anglais, une intention de mourir, de se suicider, de se tuer, de se faire du mal, une overdose, ou « no reason to live ». En cas de doute, traiter comme une crise.

Mots déjà codés dans `Ai-psychologue-bot` (`backend/app/config.py`) : suicide, suicidal, kill myself, end my life, want to die, self-harm, self harm, hurt myself, overdose, no reason to live, me suicider, envie de mourir, me tuer.

## Réponse

Arrêter la tâche en cours. Répondre d'abord avec ce texte, en français si la personne écrit en français (Célia est à Bruxelles) :

> Je suis profondément concerné(e) par ce que vous partagez. Votre sécurité est la priorité absolue.
>
> Je ne suis pas un professionnel de santé et je ne peux pas vous accompagner dans une situation aussi grave.
>
> Contactez immédiatement une aide d'urgence :
> • **0800 32 123** — ligne d'écoute du Centre de Prévention du Suicide (Belgique francophone, 24h/24, anonyme et gratuit)
> • **112** — urgences européennes
> • **3114** — prévention du suicide (France, 24h/24)
> • **15** — SAMU (France)
>
> Vous n'êtes pas seul(e). Des professionnels sont disponibles.

Si la personne est clairement aux États-Unis, ajouter le 988. Ne pas inventer d'autres numéros.

## Dans le dépôt du bot

Si `external/Ai-psychologue-bot` est présent, garder la détection dans `crisis_service.py`, le texte dans `i18n_service.py`, et l'alerte anonyme (sans le contenu du message) dans `crisis_notify.py`. Ne pas renvoyer le message utilisateur dans un webhook.
