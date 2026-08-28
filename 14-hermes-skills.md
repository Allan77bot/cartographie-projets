# PROJECT_SNAPSHOT.md — hermes-skills

## But
Repo GitHub public (`Allan77bot/hermes-skills`) de skills forgés pour **Hermes**, l'agent co-gérant d'Atelier Klar. Format `SKILL.md` compatible à la fois avec Hermes (`~/.hermes/skills/`) et Claude Code (`~/.claude/skills/`). Sert de dépôt distribuable pour installer/mettre à jour des skills sur le VPS Hostinger.

## Contenu/Stack
- 3 skills, chacun en dossier avec `SKILL.md` + `references/` (+ `scripts/` pour deux d'entre eux) :
  - `cold-email-grounded` — campagnes de cold email personnalisées : recherche prospect → séquence ancrée sur un signal → validation → push Instantly en pause (pilier acquisition, "version douce").
  - `skill-forge` — méthode/réflexe pour forger un nouveau skill (cadrer → écrire → relire à 3 angles via Claude Code → installer + tracer). À installer en premier.
  - `email-qa` — relecture anti-gaffe avant envoi : lint déterministe + audit de jugement (voix marque, structure, conformité, anti AI-slop) → verdict PASS/FAIL et gate go/no-go.
- Repo git initialisé, `.gitignore` minimal, `README.md` avec instructions d'installation/mise à jour sur le VPS.

## État actuel
Dernière activité 27 juin 2026, même jour que le montage de l'agent email marketing dans `hermesdossier`. Les 3 skills sont décrits comme forgés, poussés sur GitHub et installés/enabled sur le VPS (confirmé côté `hermesdossier/snapshot.md`).

## Ce qui est complet/incomplet
**Complet** : les 3 skills sont écrits avec leur documentation, installés sur le VPS, et le README donne une procédure claire d'installation/mise à jour.
**Incomplet** : pas de tests visibles, pas de CI ; le pilote réel (10 leads) qui doit prouver `cold-email-grounded` + `email-qa` en conditions réelles n'a pas été lancé au moment de la dernière trace connue (voir `hermesdossier`).

## Prochaines étapes probables
1. Lancer et observer le pilote de prospection qui utilise ces skills.
2. Ajuster `cold-email-grounded`/`email-qa` selon les retours du pilote.
3. Éventuellement transformer le pilote prouvé en skill `prospection-runner` pour le cron (mentionné dans `hermesdossier/snapshot.md`).

## Questions ouvertes
- Ce repo a-t-il reçu des mises à jour depuis le 27 juin (nouveaux skills, corrections) ?
- Le lien avec `hermesdossier` est-il toujours à jour, ou les deux dossiers ont-ils divergé ?
- Le repo étant public sur GitHub, une revue rapide de fuite de données/secrets a-t-elle été refaite récemment ?
