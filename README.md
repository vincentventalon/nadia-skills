# nadia-skills

Les skills Claude Code de [Nadia](https://usenadia.com) : tu dis à Claude ce que tu veux publier,
il passe par Nadia pour le faire. Toutes commencent par `nadia-` : tape `/nadia` dans Claude Code
et elles sont toutes là.

| Skill | Ce qu'elle fait |
|---|---|
| `nadia-schedule-my-post` | programme un post sur tes réseaux connectés à Nadia : lit les règles de chaque réseau, trouve le prochain créneau libre, écrit le texte de chaque plateforme, te montre le plan, et programme (ou met en brouillon) après ton « oui ». |
| `nadia-set-up-comment-to-dm` | pose l'automatisation « commente un mot → reçois le lien en DM » sur un post Instagram, au moment de le programmer ou une fois en ligne, puis vérifie qu'elle a pris. |

Rien ne part sans ton « oui » sur le plan.

## Installer

Dans Claude Code :

```text
/plugin marketplace add vincentventalon/nadia-skills
/plugin install nadia@nadia
```

## Brancher Nadia

Deux portes, au choix :

- **le connecteur Nadia** dans Claude, si tu l'as déjà ajouté : rien d'autre à faire ;
- **la CLI** : `npm install -g @usenadia/cli`, puis ta clé dans Nadia → Settings → Developers et
  `nadia auth login`. La clé est rangée dans `~/.config/nadia/credentials.json`, lisible par toi
  seul. Elle ne passe jamais par Claude, ni dans un fichier de ton projet.

MIT.
