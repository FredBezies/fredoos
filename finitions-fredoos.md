# FredoOS, les finitions !

Le plus long dans tout projet, ce sont les finitions. Voici donc quelques ajouts à faire pour rendre l’installation encore plus polyvalente et plus utilisable au quotidien.

Les finitions sont rajoutées chronologiquement, ce qui veut dire que ce document aura vocation à être modifié régulièrement.

## I) Les linux headers

Le premier paquet logiciel à rajouter, c’est le paquet linux-headers. En effet, si vous avez besoin d’installer un paquet comme un module noyau – ce à quoi j’ai été confronté récemment comme dans cet article de blog : [https://blog.fredericbezies-ep.fr/2026/09/03/ah-les-archlinuxeries/](https://blog.fredericbezies-ep.fr/2026/09/03/ah-les-archlinuxeries/) - il suffit de passer par Octopi et de rechercher le paquet linux-headers correspondant, à savoir :

- linux-headers pour le noyau linux court terme
- linux-lts-headers pour le noyau linux long terme
- linux-zen-headers pour le noyau linux zen

## II) Un bloc notes

Autre outil que j’avais oublié d’installer dans le guide officiel, c’est un bloc note quand on a besoin de créer rapidement un fichier texte. J’ai donc choisi [Featherpad](https://github.com/tsujan/featherpad) que vous pourrez ajouter à votre installation.

![FeatherPad en action](12.png)

## III) La retouche photo

Pour la retouche d’image et de photo, soit Gimp, soit Krita, ce dernier étant plus adapté aux environnements de bureau basé sur QT, comme LXQt.

![Krita en action](13.png)

## IV) SDDM et son thème

Il y a un point moche, c'est le SDDM qui nous accueille et qui est moche. Par défaut, les thèmes elarun, maya et maldives sont installés. Personnellement, j'ai choisi le paquet AUR [archlinux-themes-sddm](https://aur.archlinux.org/packages/archlinux-themes-sddm) que je trouve minimaliste et sympa.

Une fois le thème installé via yay ou octopi, on commence par créer un répertoire puis un fichier de configuration qui va nous permettre de personnaliser SDDM. On passe par la ligne de commande, c'est plus rapide et plus simple.

```
sudo mkdir -p /etc/sddm.conf.d
sudo nano /etc/sddm.conf.d/sddm.conf
``` 

Et on entre les lignes suivantes :

```
[Theme]
Current=archlinux-soft-grey
```

Vous pouvez remplacer archlinux-soft-grey par elarun, maya ou maldives. Et voici le résultat avec archlinux-soft-grey :

![SDDM en action](14.png)

