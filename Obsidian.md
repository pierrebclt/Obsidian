Backlink : [[000 HOME]]

---

J'ai expliqué le mode de fonctionnement que j'ai retenu dans [[2022-05-01#Recherche solution synchronisation avec ordinateur]]

# Fichier de type log (daté)


### Réunion 

Toutes les options ci-dessous partent du principe qu'on aura un fichier par couple *réunion/date*


#### Option 1 - la plus simple 

- Dans le daily, saisir un lien vers une réunion à créer 
	- Ex: 10h00 : [[2020-05-05 Réunion JCI supply chain TEST]]
- Ensuite dans le fichier créé indiquer un tag pour expliquer de quelle réunion il s'agit :
	- Ex : tag *meeting/jci/supply_chain*
	- C'est tout, dans JCI on met le tag pour retrouver toutes ces réunions et voilà 

#### Option 2

- Dans le daily, saisir un lien vers une réunion à créer 
	- Ex: 10h00 : [[2020-05-05 Réunion JCI supply chain TEST]]
- Ensuite dans le fichier créé indiquer un tag pour expliquer de quelle réunion il s'agit :
	- Ex : tag *meeting/jci/supply_chain*
	- Ceci pour qu'avec dataview on puisse le faire figurer dans les réunions JCI/supply chain 
- Rajouter un backlink vers les réunions génériques :
	- Ex : backlink : [[JCI - Réunions supply chain]]

#### Option 3

- Dans le daily, saisir un lien vers la réunion générique 
	- ex : 10h00 : [[JCI - Réunions supply chain]]
- Ensuite depuis la réunion générique on créé un lien vers la réunion du jour (et en plus on peut l'embded)
	- ex: - [[2020-05-05 Réunion JCI supply chain TEST]]
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
	- 


