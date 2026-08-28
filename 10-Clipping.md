# PROJECT_SNAPSHOT — Clipping

## But
Web app locale (Next.js) qui transforme une vidéo longue (podcast, interview, talk)
en clips verticaux 9:16 sous-titrés prêts pour TikTok/Reels/Shorts. Pipeline :
extraction audio FFmpeg → transcription Whisper (OpenAI) → détection des meilleurs
moments (Claude ou GPT) → preview/réglages dans le navigateur (Remotion Player) →
export MP4 1080×1920 (coupe FFmpeg + habillage Remotion, sous-titres animés mot à mot).

## Contenu / Stack
- Next.js 15 + React 19 + TypeScript, Tailwind 4.
- Remotion 4 (bundler, player, renderer, google-fonts) pour la composition vidéo.
- `@anthropic-ai/sdk` et `openai` pour la détection de moments et la transcription.
- Structure : `app/` (pages + API import/media/statut), `components/` (import, vue
  projet, carte clip avec Remotion Player), `remotion/` (composition `CaptionedClip`),
  `lib/pipeline/` (ffmpeg.ts, transcribe.ts, detect.ts, render.ts, run.ts).
- `Demarrer.bat` : lancement local en un clic (public cible : usage perso, non technique).
- Mode démo `MOCK_MODE=1` pour tester sans clé API.
- Pas de dépôt git initialisé (`git status` → "not a git repository").

## État actuel
- Dernière modif : 14 août 2026 (~2 semaines avant l'audit).
- README complet et à jour (prérequis, démarrage, structure, réglages `.env` détaillés).
- `package.json` cohérent avec le README (Next 15, Remotion 4, Anthropic/OpenAI SDK).
- `_to_delete_archive.tar.gz` (61 Ko, daté du 14 août 14:50, soit **juste avant** le
  dernier commit de code à 14:51) contient une ancienne version des mêmes fichiers
  (`components/`, `app/`, `lib/`, README, config) — c'est une sauvegarde de ménage
  avant un refactor/nettoyage, pas un signe d'abandon. Le nom indique clairement une
  intention de suppression jamais finalisée.
- Aucune trace de mise en prod / déploiement — usage local uniquement (`npm run dev`).

## Ce qui est complet / incomplet
**Complet** : pipeline bout-en-bout fonctionnel (import → transcription → détection →
preview → export), mode démo, doc d'installation, réglage du style des sous-titres via
Remotion Studio.

**Incomplet (roadmap assumée dans le README)** :
- Recadrage automatique sur le visage du speaker (MediaPipe/ClipsAI).
- Styles de sous-titres multiples.
- B-roll, hook visuel, progress bar.
- File d'attente / rendu batch de tous les clips.
- Publication directe (YouTube Shorts / TikTok API).
- Déploiement hébergé (upload, comptes, workers GPU) — reste un outil 100% local pour l'instant.

## Prochaines étapes probables
- Supprimer `_to_delete_archive.tar.gz` si le refactor est validé stable (ménage à finir).
- Initialiser un dépôt git (aucun actuellement) pour sécuriser l'historique.
- Décider si l'outil reste un usage perso local ou vise une version hébergée/multi-utilisateur.

## Questions ouvertes
- Le tar.gz peut-il être supprimé sans risque (le contenu semble redondant avec le code actuel) ?
- Le projet est-il encore utilisé activement pour découper de vraies vidéos, ou a-t-il servi
  une fois puis a été laissé de côté ?
- Un dépôt git distant existe-t-il ailleurs, ou tout le code n'existe qu'en local ?
