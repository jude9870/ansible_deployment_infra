# ansible_deployment_infra
## Description

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

A la fin du playbook créé également un hosts.ini de la vm grace a une template Jinja2 pour lancer des playbooks sur la VM: 
hosts.j2
Edit : la création hosts.ini n'a pas eu le temps d'être implémenté

## Requirement

```bash
sudo apt update
sudo apt install -y curl

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
```

## Usage

ansible-playbook creation_infra.yml

## Crédits

Judicael, Maxime, Raphael
