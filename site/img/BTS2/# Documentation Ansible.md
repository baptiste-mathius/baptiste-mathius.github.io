# Documentation Ansible - MATHIUS Baptiste

## Ansible 

- Ansible est un outil d'automatisation permettant de gérer des configurations, déployer des applications et orchestrer des tâches sur plusieurs machines. 

## Commandes Ansible 
  
- Executer une commande ad-hoc : ansible hosts -m module -a "arguments"
  
- Vérifier l'espace disque : -m shell -a "df -h"
  
- Installer un paquet : ansible all -m apt -a "name=curl state=present" -b
  
- Gérer un service : ansible all -m service -a "name=nginx state=stopped" -b
  
- Copier un fichier : ansible all -m copy -a "src=/local/path dest=/remote/path" -b
  
- Créer un répertoire : ansible localhost -m file -a "path=ansible_directory state=directory"
  
- Executer une commande dans le shell : ansible all -m command -a "uptime"
  
- Redémarrer des serveurs : ansible -a "/sbin/reboot"
  
- Activer le mode verbose pour lister les erreurs : ansible-playbook playbook.yml -vvv

- Installer sudo : apt-get install sudo

- Permition ssh pour le user root : PermittRootLogin Yes

- Génération de clé SSH : ssh-keygen 

- Copie de la clé SSH : ssh-copy-id root@ip

- Tester la connexion avec les hotes : ansible all -m ping

- Création fichier hosts : mkdir hosts && nano hosts 

- Test du playbook : ansible-playbook -i hosts premier_playbook.yml --check

- Execution d'un palybook : ansible-playbook -i hosts playbook.yml


