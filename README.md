# ansible_deployment_infra

Déploiement d'une infrastructure système/réseau à l'aide d'Ansible depuis une VM Linux vers Azure.

Liste des éléments déployés :
  - Création d'un groupe de Ressource
  - Création d'un réseau virtuel
  - Ajout d'un sous-réseau
  - Création d'une IP Publique
  - Affichage de l'IP Publique
  - Création de d'un groupe de sécurité autorisant le SSH
  - Création d'une interface réseau virtuelle associé à l'IP publique précédemment
  - Création d'une machine virtuelle Ubuntu 22_04
