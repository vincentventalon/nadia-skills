# nadia-skills

Dépôt public (MIT) des skills Claude Code de Nadia : `vincentventalon/nadia-skills`, un marketplace
`nadia`, un plugin `nadia`. Vit dans `~/Code/cockpit/nadia-skills/` (repo git à part, ignoré par le
cockpit), comme `public-skills/`.

- **Chaque skill commence par `nadia-`**, puis dit ce qu'elle fait en mots (`nadia-schedule-my-post`).
  Le dossier = le `name:` du SKILL.md.
- **Aucune clé, aucun secret.** Une skill passe par le connecteur Nadia ou par la CLI
  `@usenadia/cli` (`nadia auth login` lancé par l'utilisateur) ; jamais `--api-key` en ligne de
  commande, jamais un chemin de `_secrets/`.
- **Rien du process de Vincent** (son tableau, ses colonnes, ses comptes, ses mots-clés, ses
  liens courts) : ça reste dans les skills privées du cockpit (`nadia-carte`, `tiktok-publish`).
- Une commande citée dans une skill existe dans la CLI publiée : vérifier avec
  `npx -y @usenadia/cli@latest <commande> --help`, et `--dry-run` pour la forme de la requête.
- **Une skill ajoutée ou modifiée = la `version` du plugin monte** dans
  `.claude-plugin/marketplace.json`, sinon rien n'atteint les installés. Et le tableau du README suit.
- SKILL.md en anglais (déclencheurs FR + EN dans la description), README en français.
