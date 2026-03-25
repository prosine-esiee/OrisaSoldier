# Projet Proxmox - OrisaSoldier

## Objectif
Déployer automatiquement une VM Lubuntu sur Proxmox avec l'outil Ansible.

## Structure
- "créer_VM_playbook.yml" : Le code exécuté par Ansible pour créer une VM et la lancer sur notre environnement Proxmox
- "inventories/dev/hosts" et "inventories/prd/hosts" : Les fichiers où on sauvegarde les fichiers d'hôtes et les mots de passes.
- "inventories/dev/vars/main.yml" et "inventories/prd/vars/main.ym" : Les fichiers où on sauvegarde les variables utilisées par le playbook Ansible. Des variables telles qu'adresse IP du serveur Ansible, les identifiants "root" et le nom du noeud sur notre serveur Proxmox.

## Comment lancer ?
**Commande pour la DEV :**
```bash
ansible-playbook -i inventories/dev/hosts créer_vm_playbook.yml
```
*Pour l'environnement "prd" il faut remplacer "dev" par "prd". Taper le mot de passe SSH quand demandé.*

## Exemples d'exécution

Une capture d'exécution d'exemple est sur la racine du dépot de nom "exécution_du_playbook.png".
Une capture de la VM créée sur l'environnement Proxmox est sur la racine du dépot de nom "affichage_VM_créé_ansible.png".
