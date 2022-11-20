# ACME.SH, STOP ERROR "Client ID is not numeric" !


## DESCRIPTION (Français) [English is lower]

Ce dépot **uniquement dédié à acme.sh** et son API DNS "**dns_ispconfig.sh**" est destiné à lutter contre cette erreur récurente **Client ID is not numeric**.

Il semblerait que certains hébergeurs "bricolent" ISPCONFIG afin que des ID exclusivement numériques soient utilisés. Une abberation en matière de sécurité mais simple à gérer !..

Certains utilisateurs de **acme.sh** pensent apporter une amélioration en copiant/collant le code de leur hébergeur sur le dépôt de **acme.sh**.
Quelle erreur !
Le pire est que ce code ne semble pas être vérifié puisqu'il se retrouve à chaque fois dans un commit suivi d'une mise à jour...

La solution est simple :
* Ne plus mettre à jour **acme.sh**
* Effectuer un downgrade de **acme.sh** ou de l'API **dns_ispconfig.sh**.

La solution trouvée, la plus simple possible, est de modifier l'API **dns_ispconfig.sh** pour qu'elle cesse d'utiliser exclusivement des ID client numériques.


## UTILISATION

Récupérez le fichier API **dns_ispconfig.sh** et copiez/collez le dans le dossier **/.acme.sh/dnsapi** en écrasant le fichier posant problème.

<hr>

## DESCRIPTION (English)

This repository is only **dedicated to acme.sh** and its DNS API "**dns_ispconfig.sh**" and is intended to fight against this recurrent error **Client ID is not numeric**.

It seems that some hosting companies "tinker" with ISPCONFIG so that exclusively numeric IDs are used. An aberration in terms of security but easy to manage!

Some acme.sh users think they can improve the security by copying and pasting the code of their host into the acme.sh repository. What a mistake! The worst thing is that this code doesn't seem to be checked since it is always in a commit followed by an update...

The solution is simple:
* Don't update **acme.sh** anymore
* Downgrade **acme.sh** or the **dns_ispconfig.sh** API.

The solution found is to modify the **dns_ispconfig.sh** API to stop using only numeric client IDs.

## USE

Get the API file **dns_ispconfig.sh** and copy/paste it into the **/.acme.sh/dnsapi** folder, overwriting the problematic file.
