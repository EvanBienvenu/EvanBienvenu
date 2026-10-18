# Glossaire des termes techniques

Ce glossaire explique simplement les termes utilisés dans mon portfolio et dans mes projets. Il s'adresse aussi bien aux recruteurs qu'aux personnes qui découvrent l'informatique.

[⬅ Retour au portfolio](README.md)

## Sommaire

- [Réseau](#réseau)
- [Systèmes](#systèmes)
- [Scripting et automatisation](#scripting-et-automatisation)
- [Gestion de parc et supervision](#gestion-de-parc-et-supervision)
- [Sécurité](#sécurité)
- [Outils et DevOps](#outils-et-devops)
- [Formations](#formations)

## Réseau

| Terme | Explication |
| --- | --- |
| **Adresse IP** | Numéro qui identifie un appareil sur un réseau, comme une adresse postale. Exemple : `192.168.1.10`. |
| **Masque de sous-réseau** | Indique quelle partie de l'adresse IP désigne le réseau et quelle partie désigne l'appareil. Exemple : `255.255.255.0` (ou `/24`). |
| **LAN** | *Local Area Network* : réseau local, par exemple celui d'un bâtiment ou d'un étage. |
| **WAN** | *Wide Area Network* : réseau étendu qui relie des sites éloignés (par exemple des villes). |
| **Routeur** | Équipement qui relie plusieurs réseaux entre eux et choisit le chemin pour acheminer les données. |
| **Switch (commutateur)** | Équipement qui relie les appareils d'un même réseau local et envoie les données uniquement au bon destinataire. |
| **Cisco 1941 / 2960** | Modèles de matériel Cisco : le 1941 est un routeur, le 2960 est un switch. Très utilisés en formation. |
| **Packet Tracer** | Logiciel de Cisco qui permet de simuler un réseau complet sur ordinateur, sans matériel physique. |
| **Routage statique** | Les routes sont écrites à la main par l'administrateur. Simple, mais ne s'adapte pas tout seul en cas de panne. |
| **Routage dynamique** | Les routeurs échangent automatiquement des informations pour trouver les meilleurs chemins. |
| **RIPv2** | Protocole de routage dynamique simple, qui choisit le chemin traversant le moins de routeurs (« sauts »). Limité à 15 sauts. |
| **OSPFv2** | Protocole de routage dynamique plus performant que RIP. Il calcule le chemin le plus rapide en tenant compte du débit des liens. |
| **Topologie en anneau** | Organisation où chaque site est relié à deux voisins, formant une boucle. Si un lien tombe, le trafic peut passer par l'autre côté. |
| **VLAN** | *Virtual LAN* : découpage d'un switch en plusieurs réseaux séparés, par exemple un VLAN « Comptabilité » et un VLAN « Direction ». Améliore la sécurité et l'organisation. |
| **Routage inter-VLAN** | Permet aux différents VLAN de communiquer entre eux, en passant par un routeur. |
| **Trunk (802.1Q)** | Lien entre deux équipements qui transporte plusieurs VLAN à la fois, chaque trame étant « étiquetée » avec son numéro de VLAN. |
| **Router-on-a-stick** | Technique où un seul port de routeur, découpé en sous-interfaces, assure le routage de plusieurs VLAN. |
| **DHCP** | Service qui attribue automatiquement une adresse IP aux appareils qui se connectent au réseau. |
| **Relais DHCP (DHCP relay)** | Permet à un serveur DHCP unique de servir plusieurs réseaux : le routeur transmet les demandes au serveur. |
| **`ip helper-address`** | Commande Cisco qui active le relais DHCP sur une interface de routeur. |
| **DNS** | Service qui traduit un nom (ex. `google.fr`) en adresse IP, comme un annuaire téléphonique. |
| **ACL** | *Access Control List* : liste de règles sur un routeur qui autorise ou bloque certains flux (par adresse, protocole ou port). |
| **NAT** | *Network Address Translation* : traduit les adresses privées d'un réseau interne en adresse publique pour accéder à Internet. |
| **PAT** | *Port Address Translation* : variante du NAT où plusieurs appareils partagent une seule adresse publique, distingués par des numéros de port. C'est ce que fait une box Internet. |
| **Ping** | Commande qui teste si un appareil répond sur le réseau. |
| **Traceroute** | Commande qui affiche le chemin (la liste des routeurs) emprunté pour atteindre une destination. |

## Systèmes

| Terme | Explication |
| --- | --- |
| **Système d'exploitation (OS)** | Logiciel principal qui fait fonctionner un ordinateur : Windows, Linux, macOS… |
| **Windows Server 2022** | Version de Windows conçue pour les serveurs d'entreprise. |
| **Linux** | Système d'exploitation libre, très utilisé sur les serveurs. |
| **Debian / Ubuntu** | Deux distributions (versions) de Linux : Debian est réputée pour sa stabilité sur les serveurs, Ubuntu en est dérivée. |
| **SSH** | Protocole qui permet d'administrer un serveur à distance, en ligne de commande, de façon chiffrée. |
| **root** | Le compte administrateur tout-puissant de Linux. |
| **Active Directory (AD DS)** | Annuaire de Microsoft qui centralise les comptes utilisateurs, les ordinateurs et les droits d'accès d'une entreprise. |
| **Machine virtuelle (VM)** | Ordinateur simulé par un logiciel, qui fonctionne à l'intérieur d'un vrai ordinateur. Permet de faire tourner plusieurs systèmes sur une seule machine. |
| **HDD / SSD** | Deux types de disques de stockage : le HDD est mécanique, le SSD est électronique et bien plus rapide. |
| **RAM** | Mémoire vive : mémoire rapide et temporaire utilisée par l'ordinateur pendant son fonctionnement. |

## Scripting et automatisation

| Terme | Explication |
| --- | --- |
| **Script** | Petit programme qui automatise une suite de tâches répétitives. |
| **Bash** | Langage de script des systèmes Linux. |
| **PowerShell** | Langage de script de Microsoft, utilisé pour administrer Windows et Active Directory. |
| **Python** | Langage de programmation polyvalent, très utilisé pour l'automatisation. |
| **JavaScript** | Langage de programmation principalement utilisé pour les sites web. |
| **CSV** | Fichier texte en forme de tableau, où les valeurs sont séparées par des virgules ou des points-virgules. Souvent utilisé pour importer des listes d'utilisateurs. |
| **API REST** | Moyen standard pour que deux logiciels communiquent entre eux via le web (par des requêtes HTTP). |
| **SHA-256** | Algorithme qui calcule l'« empreinte » unique d'un fichier. Si le fichier est modifié, même d'un seul caractère, l'empreinte change : on vérifie ainsi qu'il n'a pas été altéré. |

## Gestion de parc et supervision

| Terme | Explication |
| --- | --- |
| **Gestion de parc** | Suivi de l'ensemble du matériel et des logiciels d'une organisation. |
| **GLPI** | Logiciel libre de gestion de parc et de suivi des tickets d'incident (helpdesk). |
| **Ticket d'incident** | Demande enregistrée lorsqu'un utilisateur rencontre un problème, pour en suivre la résolution. |
| **Agent GLPI** | Petit programme installé sur chaque machine, qui envoie automatiquement son inventaire au serveur GLPI. |
| **LDAP** | Protocole qui permet à une application (comme GLPI) d'interroger un annuaire (comme Active Directory). |
| **WAPT** | Logiciel qui installe et met à jour automatiquement des programmes sur de nombreux ordinateurs à la fois. |
| **Packaging** | Préparation d'un logiciel sous forme de « paquet » prêt à être installé automatiquement. |
| **Déploiement multi-OS** | Installation de logiciels ou de configurations sur des ordinateurs utilisant des systèmes différents (Windows, Linux, macOS). |
| **Supervision** | Surveillance en continu des serveurs et équipements pour détecter les pannes ou les ralentissements. |
| **Centreon** | Logiciel de supervision qui affiche l'état des équipements et envoie des alertes en cas de problème. |
| **Métrique** | Valeur mesurée régulièrement : utilisation du processeur, espace disque, temps de réponse… |

## Sécurité

| Terme | Explication |
| --- | --- |
| **ANSSI** | Agence nationale de la sécurité des systèmes d'information : l'organisme français de référence en cybersécurité, qui publie des guides de bonnes pratiques. |
| **CERT-FR** | Centre gouvernemental français qui publie des alertes sur les failles de sécurité. |
| **Durcissement (hardening)** | Ensemble de réglages qui réduisent les risques d'attaque sur un système : désactiver l'inutile, limiter les droits, appliquer les mises à jour. |
| **Gestion des droits** | Définir qui peut lire, modifier ou exécuter chaque fichier ou ressource. |
| **Pare-feu (firewall)** | Filtre qui autorise ou bloque le trafic réseau selon des règles. |
| **iptables / nftables** | Outils de pare-feu intégrés à Linux. nftables est le successeur moderne d'iptables. |
| **Veille technologique** | Activité qui consiste à se tenir régulièrement informé des nouveautés et des menaces dans son domaine. |

## Outils et DevOps

| Terme | Explication |
| --- | --- |
| **Docker** | Outil qui fait tourner des applications dans des « conteneurs » isolés, faciles à déployer et à reproduire. |
| **Conteneur** | Environnement léger et isolé qui contient une application et tout ce dont elle a besoin pour fonctionner. |
| **Docker Compose** | Outil qui décrit et lance plusieurs conteneurs à partir d'un seul fichier de configuration. |
| **MySQL** | Système de gestion de bases de données très répandu. |
| **MariaDB** | Système de gestion de bases de données compatible avec MySQL, installé par défaut sur Debian. |
| **LAMP** | Ensemble de logiciels pour héberger une application web : Linux, Apache, MariaDB/MySQL, PHP. |
| **Apache** | Serveur web : il reçoit les requêtes des navigateurs et renvoie les pages. |
| **PHP** | Langage de programmation exécuté par le serveur web, utilisé notamment par GLPI. |
| **Git** | Logiciel de gestion de versions : il garde l'historique de toutes les modifications d'un projet. |
| **GitHub** | Site web qui héberge des projets Git et permet de les partager. |
| **Dépôt (repository)** | Dossier d'un projet suivi par Git, avec tout son historique. |
| **DevOps** | Démarche qui rapproche les développeurs (Dev) et les administrateurs (Ops) pour livrer plus vite et plus fiablement, notamment grâce à l'automatisation. |

## Formations

| Terme | Explication |
| --- | --- |
| **BTS SIO** | Brevet de technicien supérieur « Services Informatiques aux Organisations » (Bac+2). |
| **Option SISR** | « Solutions d'Infrastructure, Systèmes et Réseaux » : l'option du BTS SIO tournée vers l'administration réseau et système. |
| **Bac pro SN option RISC** | Bac professionnel « Systèmes Numériques », option « Réseaux Informatiques et Systèmes Communicants ». |
| **Alternance** | Formation qui alterne périodes à l'école et périodes en entreprise. |
