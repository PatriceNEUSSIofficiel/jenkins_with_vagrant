# jenkins_with_vagrant

# Configuration Vagrant pour p1jenkins-pipeline

Ce projet Vagrant fournit une configuration pour créer une machine virtuelle Vagrant avec le nom "p1jenkins-pipeline" basée sur l'image "debian/buster64". Cette machine virtuelle sera configurée avec une adresse IP privée de 192.168.5.2. Le fichier `install_p1jenkins.sh` sera exécuté en tant que provisionnement pour effectuer des installations supplémentaires.

## Prérequis

Avant de pouvoir utiliser cette configuration Vagrant, assurez-vous d'avoir installé les éléments suivants sur votre système :

- [Vagrant](https://www.vagrantup.com/downloads)
- [VirtualBox](https://www.virtualbox.org/wiki/Downloads)

## Configuration

La configuration Vagrant est définie dans le fichier `Vagrantfile`. Voici les principales caractéristiques de la configuration :

- Le nom de la machine virtuelle est défini comme "p1jenkins-pipeline".
- L'image de la machine virtuelle utilisée est "debian/buster64". Si l'image n'est pas déjà téléchargée, Vagrant la téléchargera automatiquement.
- La machine virtuelle sera configurée avec une adresse IP privée de 192.168.5.2.
- La machine virtuelle sera provisionnée en exécutant le script `install_p1jenkins.sh`.
- La configuration de VirtualBox inclut des personnalisations pour la machine virtuelle, telles que la mémoire (3072 Mo), le nom et le nombre de CPU (1).

## Utilisation

1. Assurez-vous que vous avez satisfait aux prérequis en installant Vagrant et VirtualBox sur votre système.
2. Clonez ce dépôt ou créez un fichier Vagrantfile avec le contenu fourni.
3. Ouvrez un terminal et naviguez jusqu'au répertoire contenant le fichier Vagrantfile.
4. Exécutez la commande `vagrant up --provider=virtualbox` pour démarrer la machine virtuelle.
5. Attendez que Vagrant crée et provisionne la machine virtuelle. Cela peut prendre quelques minutes.
6. Une fois le processus terminé, vous pouvez vous connecter à la machine virtuelle en utilisant la commande `vagrant ssh` ou en utilisant un client SSH de votre choix avec les informations suivantes :
   - Hôte : 192.168.5.2
   - Nom d'utilisateur : vagrant
   - Mot de passe : vagrant

N'hésitez pas à personnaliser la configuration selon vos besoins en modifiant le fichier Vagrantfile ou en ajoutant d'autres scripts de provisionnement.

## Auteur

Ce projet Vagrant a été créé par [Votre Nom](https://github.com/votre-utilisateur).