# Table de l'Entaille — jouer à distance

Une page publiée sous le compte d'Alex, pour qu'un joueur à distance participe à une séance
du Monde de l'Entaille depuis son iPhone :
https://claude.ai/artifact/3NbNyVZZK7NgUZX5jXiqEd

Le joueur ne parle jamais à Claude et n'a aucun fichier à gérer. Il ouvre un lien, choisit
son personnage une fois, puis à chaque tour il lit le récit, écrit son action et appuie sur
« Envoyer au MJ ». Tout le reste (dés, fichiers, secrets, arbitrage) reste dans la séance
Cowork d'Alex.

## Ce que voit le joueur

- le dernier tour du récit, mis à jour tout seul, et les tours précédents ;
- une barre d'état : « À toi, Fifi », « Le MJ raconte », « Partie en pause » ;
- un champ pour son action, et « Je passe ce tour » ;
- ses billets, que lui seul peut lire ;
- sa fiche (chiffres publics) ;
- un message privé au MJ, que personne d'autre ne lit.

Alex, propriétaire de la page, voit en plus la « Vue du MJ » pour confirmer qui joue qui.
Il ne voit jamais les billets ni les messages privés, parce qu'il joue aussi.

## Mise en place (Alex)

1. Ouvre la page, menu **Partager**, invite l'adresse e-mail Claude du joueur avec le rôle
   **Éditeur**. N'active **aucun lien de partage** : un invité extérieur à ton organisation
   ne peut écrire que s'il est Éditeur et que la page n'est pas partagée par lien.
2. Envoie-lui le message ci-dessous.
3. Quand il a choisi son personnage, ouvre la page. Dans « Vue du MJ », appuie sur
   **Confirmer** en face de son nom.
4. Importe les deux compétences mises à jour, prêtes dans `competences/`
   (`maitre-du-jeu.zip`, `monde-entaille.zip`) : Personnaliser → Compétences → Ajouter →
   Importer, « Téléverser et remplacer ». Range aussi les deux `.zip` dans
   `jdr/_competences/`.
5. Mets à jour `campagnes/les-cendres-de-valdreth/table.md`, section « Comment se déroule
   une séance » : qui joue à distance, par la page, et comment lui passent les billets.
6. Fais un essai avant la vraie séance. Il choisit son personnage, tu confirmes, Claude
   écrit un tour et un billet d'essai. Il doit voir les deux, et un autre compte ne doit
   pas voir le billet.

## Message à envoyer au joueur

> Tu vas recevoir un e-mail d'invitation de Claude. Ouvre le lien sur ton iPhone et
> connecte-toi avec cette adresse-là.
>
> La première fois, choisis ton personnage et appuie sur « C'est moi ». Je confirme de mon
> côté, et la page s'ouvre sur la partie.
>
> Pendant la partie, lis le dernier tour en haut. Quand la barre dit « À toi », écris ce que
> fait ton personnage, comme tu le dirais à voix haute, et appuie sur « Envoyer au MJ ». La
> suite arrive toute seule, pas besoin de recharger.
>
> Astuce : dans Safari, bouton Partager puis « Sur l'écran d'accueil », pour retrouver la
> page comme une appli.

La page ne transporte pas la voix. Pour suivre ce qui se dit à la table, un appel en parallèle
(FaceTime, Discord) reste utile.

## Pourquoi pas un fichier à déposer dans sa conversation

Un fichier déposé dans la conversation du joueur donnerait des consignes à *son* Claude, sur
*son* compte. Ce Claude n'a accès ni au dossier `jdr`, ni aux dés d'Alex, ni à l'état de la
partie. Il deviendrait un second MJ qui ne sait rien, ou il faudrait qu'il manipule lui-même
la page, avec des outils que l'application du joueur n'a pas forcément. Le lien est plus
simple pour un débutant : aucune conversation Claude, un seul bouton.

## Modifications des compétences

Déjà faites dans les deux `.zip` de `competences/`, construits à partir des versions
installées le 26/09/2026. Pour mémoire, dans `maitre-du-jeu/SKILL.md`, tableau § 8, ajouter :

```
| Un personnage joué à distance, par la page de table | `references/table-a-distance.md` |
```

Dans `monde-entaille/SKILL.md`, section « Ce qui ne s'affiche jamais », remplacer la première
phrase par :

```
**La table de Valdreth joue autour d'un seul écran : Alex lit à voix haute et joue Casimir.
Un joueur peut jouer à distance par la page de table (`references/table-a-distance.md`) :
ses billets passent par la page, jamais par l'écran d'Alex. Alex joue aussi, seul,
*Ce qui est tombé du ciel*.** Tout ce que tu écris peut être lu.
```

Puis, pour chaque compétence : copie dans un dossier temporaire, édition, `.zip` sous le même
nom, rangé dans `jdr/_competences/`, import par Personnaliser → Compétences → Ajouter →
Importer, « Téléverser et remplacer ».

## Limites connues

- Claude ne réagit pas seul quand le joueur écrit. C'est Alex qui lance chaque tour.
- Un Éditeur peut republier la page. Il pourrait donc en théorie changer ses règles d'accès
  et lire les billets des autres. Le secret des billets repose sur la confiance envers les
  joueurs invités.
- Les règles d'accès ont été vérifiées au niveau Éditeur, mais pas encore avec un vrai second
  compte. D'où l'essai du point 6.
- Le texte d'un billet ou d'un message privé passe par un appel d'outil dans la séance
  d'Alex. Le protocole le fait écrire et lire par un agent, pour qu'il ne s'affiche pas sur
  son écran.
- 5 000 documents au maximum dans la page. Le protocole dit quand faire le ménage.

## Fichiers

- `table.html` : la source de la page publiée.
- `protocole-mj.md` : ce que Claude fait, côté Alex, à chaque séance avec un joueur à
  distance.
- `competences/` : `maitre-du-jeu.zip` (avec `references/table-a-distance.md`) et
  `monde-entaille.zip`, prêts à importer.
