Toolbox Projet
Ce projet contient une série d'outils pour effectuer des scans de sécurité, des attaques par force brute SSH, et générer des rapports PDF des résultats de scans. Ce guide vous expliquera comment installer et utiliser chaque script.

## Prérequis

Kali Linux 024.1 (recommandation)

Python 3.11.8 (recommandation)

- Dépendances Python :
  - `reportlab`
  - `gvm` (normalement compris avec l'installation d'OpenVas)
  - `lxml`
  - `paramiko`
- Outils externes :
  - `rustscan 2.2.3` (recommandation)
  - `OpenVAS 22.7.9` (recommandation)


Dépendances Python
Installez les bibliothèques Python nécessaires avec les commandes suivantes :
pip install reportlab
pip install gvm lxml
pip install paramiko

- RustScan :
Installez RustScan avec la commande suivante :
`sudo apt-get install rustscan`

- OpenVAS :
Pour installer OpenVAS, suivez les instructions détaillées dans les liens suivants :

Guide d'installation OpenVAS sur Kali Linux :

https://www.ceos3c.com/security/install-openvas-kali-linux/

https://www.youtube.com/watch?v=OUiRTv4Q80c

## Structure du projet :

  - main.py : Script principal pour le scan OpenVAS.
  - CODE/passwordtest.py : Script de test des mots de passe.
  - CODE/rustscan_scan.py : Script pour lancer et traiter les scans RustScan.
  - CODE/ScanMachine.py : Script de gestion de la machine de scan.
  - CODE/sshbrut.py : Script pour effectuer des attaques par force brute SSH.
  - NEED/password.txt : Liste de mots de passe pour les tests de force brute.
  - NEED/user.txt : Liste de noms d'utilisateur pour les tests de force brute.

Pour lancer la toolbox, exécutez simplement le main.py. RAPPEL : SI VOUS AVEZ INSTALLÉ LA TOOLBOX DANS UN AUTRE EMPLACEMENT QUE LE BUREAU DE L'UTILISATEUR KALI, MODIFIEZ LES DIFFÉRENTS CHEMINS DES SCRIPTS.

## Rappel pour les script ScanMachine et brute force SSH

- Mettez à jour le fichier CODE/ScanMachine.py avec les informations de configuration nécessaires suivant si nécéssaire :
  - "openvas_socket"
  - "openvas_username"
  - "openvas_password"
  - "scanner_id"
    

- Attaque par force brute SSH :
  - Assurez-vous que les fichiers NEED/user.txt et NEED/password.txt contiennent les noms d'utilisateur et mots de passe à tester.
  - 

 ## Problèmes courants et solutions

- **Erreur d'installation de dépendances :** Vérifiez que vous utilisez la version recommandée de Python et de Kali Linux.
- **Problèmes de connexion OpenVAS :** Assurez-vous que vos informations de configuration dans `ScanMachine.py` sont correctes et que le service OpenVAS est en cours d'exécution.
- **Échec des scans RustScan :** Vérifiez que RustScan est correctement installé et accessible depuis votre terminal.

Pour toute autre question ou problème, veuillez consulter la documentation officielle des outils ou me contacter directement.


## Avertissement
Utilisez ces outils uniquement sur des systèmes pour lesquels vous avez l'autorisation explicite de tester la sécurité. Toute utilisation non autorisée est illégale et contraire à l'éthique.

## Auteur
Benjamin GHAZANI

## Licence
GNU General Public License v3.0
