[[000 HOME]]

---

#### A faire
Regarder comment résoudre les problèmes de conflits dans git :
- https://komodor.com/learn/how-to-fix-fatal-refusing-to-merge-unrelated-histories-error/

 A regarder la vidéo de Nick:
 https://www.youtube.com/watch?v=WUq8Pun28FI
 

#### Extensions interessantes
- [[Extensions obsidian.msg]]


# Réflexion du 10 mai

Mes remarques :
- Workflow actuel pour le daily :
	- Lien vers les réunions avec pour chaque réunion un fichier du genre "YYYY-MM-DD ma réunion"
	- J'indique dans le log les fichiers reçus des différentes personnes
- Analyse du worflow daily actuel :
	- Si dans un fichier par client ou personne ou réunion on veut regrouper en automatique tout ce qu'il y a eu, cela va représenter une liste très conséquente
	- Une autre approche serait que pour une réunion, on indique la date de telle sorte qu'en autoamatique dans le daily on puisse l'avoir (cela automatise cet aspect) => à tester tout de suite
	- Si cela marche, les pièces jointes envoyées par les personnes pourraient être centralisés auprès des personnes
	- Note : dans le cas des infos récupérées en automatique, si à un moment il y a en a trop il suffit de renommer le trigger qui pose problème
- <b>Feedback suite à essais du jour :</b>
	- Un tag précis doit permettre de remonter la liste dans la note considérée. Exemples ci-dessous.
	- tag **meeting/2022-05-10** : permet de remonter dans la note 2022-05-10 toutes les réunions qui ont eu lieu ce jour
	- tag **meeting/jci/supply_chain** : permet de remonter dans JCI la liste de toutes les réunions supply chain. Note: si on en a trop à un moment, à la fin de l'année il suffira de renommer ces réunions en ajoutant l'année qui vient de s'écouler. exemple: meeting/2022/jci/supply_chain





---
#### Introduction

J'ai expliqué le mode de fonctionnement que j'ai retenu dans [[2022-05-01#Recherche solution synchronisation avec ordinateur]]

# Fichier de type log (daté)


### Réunion 

Toutes les options ci-dessous partent du principe qu'on aura un fichier par couple *réunion/date*


#### Option 1 - la plus simple 

- Dans le daily, saisir un lien vers une réunion à créer 
	- Ex: 10h00 : [[2022-05-05 Réunion JCI supply chain TEST]]
- Ensuite dans le fichier créé indiquer un tag pour expliquer de quelle réunion il s'agit :
	- Ex : tag *meeting/jci/supply_chain*
	- C'est tout, dans JCI on met le tag pour retrouver toutes ces réunions et voilà 

#### Option 2

- Dans le daily, saisir un lien vers une réunion à créer 
	- Ex: 10h00 : [[2022-05-05 Réunion JCI supply chain TEST]]
- Ensuite dans le fichier créé indiquer un tag pour expliquer de quelle réunion il s'agit :
	- Ex : tag *meeting/jci/supply_chain*
	- Ceci pour qu'avec dataview on puisse le faire figurer dans les réunions JCI/supply chain 
- Rajouter un backlink vers les réunions génériques :
	- Ex : backlink : [[JCI - Réunions supply chain]]

#### Option 3

- Dans le daily, saisir un lien vers la réunion générique 
	- ex : 10h00 : [[JCI - Réunions supply chain]]
- Ensuite depuis la réunion générique on créé un lien vers la réunion du jour (et en plus on peut l'embded)
	- ex: - [[2022-05-05 Réunion JCI supply chain TEST]]
- Pour que la boucle soit bouclée, dans le fichier de réunion créé faire un lien vers la date du jour :
	- [[2022-05-03]]


### Email

tag : *email/ramdane_lateb*

### Email avec attachment

#### Option  - la plus simple 

Dans le daily, saisir un lien vers le fichier où on expliquera la PJ
	- [[2022-05-06 Frédéric Ponson attach ppt sur Tamturbo]]
- Ensuite dans le fichier créé indiquer un tag pour expliquer de quelle PJ il s'agit :
	- Ex : tag *attach/frederic_ponson* et un lien vers [[Tamturbo]]
	- C'est tout, si dans *Frederic Ponson* et *Tamturbo* on a les tags on retrouvera ces infos

### 1on1

Dans le daily, saisir un lien vers le fichier de saisie des infos du 1à1
	- [[2022-05-06 1à1 avec JDT]]
- Ensuite dans le fichier créé indiquer un tag pour expliquer de quelle PJ il s'agit :
	- Ex : tag *1on1/jean-charles_dupont*
	- C'est tout, si dans *Jean-Charles Dupont* on a le tag on accédera facilement aux réunions


## Conclusion
Dans le daily, plus le lien est explicite avec les bons mots clés plus ça sera facile à retrouver 

=======
[[+Home]]

# Obsidian
Nous allons expliquer dans ce fichier comment saisir les informations

## Réunions 
- C'est un fichier de daté (de type log)
- Dans le daily, saisir un lien vers une réunion à créer 
	- Ex: 10h00 : [[2022-05-05 Réunion JCI supply chain TEST]]
- Ensuite dans le fichier créé indiquer un tag pour expliquer de quelle réunion il s'agit :
	- Ex : tags :: *tag_meeting/jci/supply_chain*
	- C'est tout, dans *JCI* on met le tag pour retrouver toutes ces réunions et voilà 
- S'il y a un compte-rendu, on vient le rajouter dedans et dans le log du daily on référence cette réunion

## 1on1
- Comme pour les *réunions*
- Tag de type *1on1/jean-charles_dupont* 


## Log d'informations
### Saisie des informations
- **Attachment :** on saisit le *tag de la personne*, *attach*, le *type d'attachment (ex:#pdf)*, et d'autres tags si besoin de donner plus de sens
	- Ex :  *jean-charles_dupont* attach #pdf *SiebAndMeyer* *Drive* *presentation* : [[SIEB&MEYER_Presentation_04_2022.pdf]]
- **Email :** Idem que pour **Attachment** sauf qu'on indique *email* et qu'il n'y a pas de type de PJ

### Important
- Si le contenu nécessite plus d'une ligne, ouvrir un fichier spécifique pour détailler le contenu

### Recherche des informations
Il suffira de faire *line:(#jean-charles_dupont attach pdf)*


---
# Fichier de type MOC

Au travail on va retrouver par exemple :
- client (ex: JCI)
- projet (ex: MBx)
- market (ex: nuclear)
- prospect (ex: Snowman)

## Fonctionnement 

Ces fichiers vont référencer :
- des tags (ex: *meeting/JCI/management_meeting*, )
- des liens vers des fichiers MOC (ex: [[JCI contracts]])
- des liens vers des fichiers log (ex :  [[2022-05-06 Frédéric Ponson attach ppt sur Tamturbo]])




# Divers

J'ai expliqué le mode de fonctionnement que j'ai retenu dans [[2022-05-01#Recherche solution synchronisation avec ordinateur]]

Utilisation de dataview et embed les résultats :
https://github.com/blacksmithgu/obsidian-dataview/issues/177

## Quelques bonnes pratiques

- Utilisation de formules
	- Exemple : $n^2$  ou encore $c_p = {a+3}/b$ 

- Raccourcis choisis pour monter ou baisser une ligne
	- Alt + Down : Descendre la ligne sélectionnée
	- Alt + up : Monter la ligne sélectionnée
	- Ctrl + Shift + V : Split vertical
	- Ctrl + Shift + H : Split Horizontal

- Mettre son propre repère dans un fichier avec le symbole '^' ^bc
	- Ex : ^ab
	- Voici le contenu et on pourra le référencer ailleurs avec MonFichier^ab

## How-to

- Search : https://help.obsidian.md/Plugins/Search
	- Voir aussi [[Regex]]
- Utilisation de Templater et de Daily (pour mettre jour d'avant et après) :
	- https://kevinquinn.fun/blog/get-started-with-obsidian-periodic-notes-and-templater/
	- https://benenewton.medium.com/my-obsidian-daily-note-template-a4bdab53dc62
- Limit of Zettelkasten for work (seems reasonnable to me and to look more in details) :
	- https://www.thoughtasylum.com/2021/07/03/i-do-not-use-zettelkasten/
	- https://www.thoughtasylum.com/2021/12/17/the-ubiquitous-linking-manifesto/
	- https://linkingmanifesto.org/motivation/

Recherche de sujets intéressants sur Obsidian 

*Templates :*
https://filipedonadio.com/6-useful-templates-for-obsidian/

*Tag pane plugin* to filter search
https://jackiegeek.gitee.io/obsidian-docs/fr/How%20to/Work%20with%20Tags/

*Quelques plugin :*
- Calendar
- Dataview
- templates
- Kanban
- Task
- 


*Meeting note in Daily Note*
Every morning when I create the Daily Note, I put all of today’s meetings in the section Meetings, with a dedicated link ([[2022-02-18 — Meeting about Project y]]) to a note about that meeting. Meetings for tomorrow (or even later) go into the FutureMeetings subheading, with links ([[2022-03-01 — Meeting on Project g]]), as well.

*Creer des master document en utilisant ! Devant le lien:*
Voir explication sur le site ci-dessous
https://jamierubin.net/2022/03/15/practically-paperless-with-obsidian-episode-22-daily-notes-revisited-the-best-of-both-worlds/

Test :
![[un]]

![[Deux]]

*Un certain nb de conseils intéressants*
- Nommer les fichiers avec zettelkasten prefixer
	https://jamierubin.net/2021/11/09/practically-paperless-with-obsidian-episode-6-tips-for-naming-notes/
- scanner les documents une fois par semaine 
	https://jamierubin.net/2021/11/02/practically-paperless-with-obsidian-episode-5-scanning-documents-into-obsidian/
- how to organise notes
	https://jamierubin.net/2022/02/15/practically-paperless-with-obsidian-episode-18-how-i-organize-my-notes/
- Tous les liens 
	https://jamierubin.net/blog-series/practically-paperless-with-obsidian/


<<<<<<< HEAD
=======
# Solutions écartées

[[Obsidian - solutions écartées]]
>>>>>>> 6e2c131130b13f0c1264ab7f7acf75d52354d541
