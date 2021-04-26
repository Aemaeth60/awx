# Rôle Ansible: Générer un mot de passe aléatoire pour un utilisateur

Ce rôle permet de générer un mot de passe aléatoire pour un utilisateur donné.
Il affiche les mots de passe générés dans la boîte dialogue Ansible/AWX et enregistre les mots de passe sur la machine de contrôle

## Pré-requis

Aucun.

## Variables du rôle

```

dest_dir: /tmp/list_passwd #fichier de destination pour l'ensemble des logins/mdp associés à la machine

```

## Example de Playbook

```

- hosts: all

  roles:
    - rand_pwd
```

Variables à définir:

```
u_name: toto #utilisateur existant 

ip_control: 10.10.0.213  #IP de la machine de contrôle


#login pour les accès à la machine
login_control: root 
passwd_control: root 
```


## Crédits

Vincent Yucel, Planet Bourgogne, 2018.
