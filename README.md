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

# ansible_deployment_infra

## Description

Playbook ansible pour creer des ressources Azure : 

- ressourcegroup

- virtual network

- subnet

- public IP

- Network Security Group

- Virtual NIC

- VM

A la fin du playbook créé également un hosts.ini de la vm grace a une template Jinja2 pour lancer des playbooks sur la VM: 
hosts.j2

## Requirement

sudo apt update -y

sudo apt install curl

curl -LsSf https://astral.sh/uv/install.sh | sh

uv python install

uv venv ansible_ipi

uv venv ansible_ipi --seed

source ansible_ipi/bin/activate

uv python install 3.13

uv python pin 3.13

uv pip install ansible

ansible-galaxy collection install azure.azcollection

uv pip install -r ~/.ansible/collections/ansible_collections/azure/azcollection/requirements.txt


## Usage

ansible-playbook azure.yaml

