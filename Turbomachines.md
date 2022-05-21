[[+Home]] > [[Knowledge MOC]]

#### Actions
- [ ] Proposer une nouveau template à remplir par les clients sur la base du mail d'Askar à Airproducts ci-dessous et des inputs annoncées dans le livre sur les turbomachines
- [ ] Voir avec Ramdane et Joaquim si on investit dans CFTurbo et si on prend une ressource pour calculer les points de fonctionnement de nos machines par application marché


## Résumé du livre Turbomachinery Springer
- Lien vers le livre en pdf : [lien)](file:///C%3A%5CUsers%5CBOUCULAT%5COneDrive%20-%20SKF%5CDocuments%5C2022%5CPerso%5CTurbomachines%5CTurbomachinery%20(Springer%20Tracts%20in%20Mechanical%20Engineering).pdf)

#### Vitesse specifique 
Page 157 - chapitre 2.3 Selection process
Pour 2 machines identiques (même vitesse spécifique), on va avoir la **Vitesse (n) x Puissance ^0.5 constant**. La puissance car on a puissance ≈ volumetric flow rate

![[Pasted image 20220519114528.png]]

#### Lien entre puissance et et compressor throughput

Source : https://myengineeringtools.com/Compressors/Tools_Compressor_Power.html
On voit que P (en kW) est proportionnel à Q le mass flow rate (en kg/s)
Or plus bas on voit que Q = rho x V avec Q le mass flow rate, rho la densité (kg/m3), et V le volumetric flow rate (en m3/s)
**Conclusion :** On a P x alpha = V, donc *V^1/2 = P^1/2 x une constante*, et donc dans la vitesse spécifique si omega_s la vitesse spécifique est constante, pour un meme paramètre de compression on aura *vitesse de rotation x puissance^1/2* qui sera constante

![[Pasted image 20220520084742.png]]

Source : https://www.ohio.edu/mechanical/thermo/Intro/Chapt.1_6/Chapter4a.html
![[flow_eqns.gif]]
## Mon analyse de l'échange avec Ethan de rotoflow

Extrait du mail d'Askar le 19.05.2022 : [[RE_ _External_ RE_ Rotoflow Bearing Applications.msg]]
Tableau issu de ce mail :
![[Pasted image 20220519115134.png]]

On voit que :
- *Puissance^0.5 x vitesse* ≈ 660K = *constante ∝ vitesse spécifique*
- Puissance x *Weight*  ≈ 34K = *constante* (commentaire Tamturbo : même vitesse et même pressure ratio= même poids - voir [[2022-05-17 Management meeting with Tamturbo| ce compte-rendu]])
- *CG* ∝ Weight
- *Thrust load* ∝ puissance

## Mon point de vue partagé avec Joaquim et Ramdane

- Mon [[CFturbo et livre turbomachines.msg|email]]
