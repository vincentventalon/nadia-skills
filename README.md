# Nadia pour Claude Code

Le plugin Claude Code de **[Nadia](https://usenadia.com/?utm_source=github&utm_medium=readme&utm_campaign=nadia-skills)**,
l'outil qui programme tes posts sur Instagram, TikTok, LinkedIn, X, Threads, Facebook et YouTube,
et qui répond à ta place à ceux qui commentent un mot. Tu dis à Claude ce que tu veux publier, il
passe par Nadia pour le faire.

Toutes les skills commencent par `nadia-` : tape `/nadia` dans Claude Code et tu les as toutes.

| Skill | Ce qu'elle fait |
|---|---|
| `nadia-schedule-my-post` | programme un post sur tes comptes habituels. La première fois, elle te montre tes workspaces et leurs comptes et tu choisis où tu postes d'habitude : c'est ton profil, elle ne redemande plus. Elle lit les règles de chaque réseau, trouve le prochain créneau libre, écrit le texte de chaque plateforme. Sur Instagram, elle te liste tes automatisations « commente un mot → DM » (la même qu'un post récent, un de tes templates, ou aucune) et te demande laquelle poser. Après ton « oui », le post et son automatisation partent d'un coup. |
| `nadia-set-up-comment-to-dm` | pose l'automatisation « commente un mot → reçois le lien en DM » sur un post Instagram déjà en ligne, vérifie qu'elle a pris, et te dit qui a reçu le DM. |

Rien ne part sans ton « oui » sur le plan.

## Installer

Dans Claude Code :

```text
/plugin marketplace add vincentventalon/nadia-skills
/plugin install nadia@nadia
```

Pour les mises à jour : `/plugin marketplace update nadia`.

## Brancher Nadia

Il te faut un compte Nadia ([les offres](https://usenadia.com/pricing?utm_source=github&utm_medium=readme&utm_campaign=nadia-skills))
avec tes réseaux connectés. Ensuite, une des deux portes :

- **La CLI** (recommandée) :

  ```sh
  npm install -g @usenadia/cli
  nadia auth login
  ```

  Ta clé se prend dans Nadia → Settings → Developers
  ([la doc](https://usenadia.com/docs/general/settings/developers?utm_source=github&utm_medium=readme&utm_campaign=nadia-skills)).
  `nadia auth login` la range dans `~/.config/nadia/credentials.json`, lisible par toi seul. Elle
  ne passe jamais par Claude, ni dans un fichier de ton projet.
  [Doc de la CLI](https://usenadia.com/docs/cli/introduction?utm_source=github&utm_medium=readme&utm_campaign=nadia-skills).
- **Le serveur MCP de Nadia**, si tu l'as déjà branché dans Claude : les skills s'en servent
  directement. [Le brancher](https://usenadia.com/docs/mcp/setup?utm_source=github&utm_medium=readme&utm_campaign=nadia-skills).

## Ton profil de publication

La première fois que tu programmes un post, `nadia-schedule-my-post` te demande où tu postes
d'habitude (un workspace entier, ou seulement certains de ses comptes), ton fuseau horaire, et si
tes posts partent programmés ou en brouillon. C'est rangé dans `~/.config/nadia/profiles.json`, ou
dans `.nadia/profiles.json` d'un projet qui poste sur ses propres comptes. Ce fichier ne contient que
des noms et des identifiants, aucune clé. Tu as plusieurs marques ? Un profil par workspace, et tu
dis « sur le compte du client » quand ce n'est pas celui par défaut. Pour le changer : « change mes comptes
par défaut ».

## Pour aller plus loin

- [Les automatisations commentaire → DM](https://usenadia.com/docs/general/automations/comment-dm?utm_source=github&utm_medium=readme&utm_campaign=nadia-skills)
- [Les créneaux de publication](https://usenadia.com/docs/general/channels/time-slots?utm_source=github&utm_medium=readme&utm_campaign=nadia-skills)
- [Nadia avec un agent](https://usenadia.com/docs/general/agents?utm_source=github&utm_medium=readme&utm_campaign=nadia-skills)
- [L'API publique](https://usenadia.com/docs/public-api/introduction?utm_source=github&utm_medium=readme&utm_campaign=nadia-skills)

Fait par [Vincent Ventalon](https://vincentventalon.com), qui s'en sert tous les jours pour ses
propres vidéos. MIT.
