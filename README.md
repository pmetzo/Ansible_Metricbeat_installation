Agent d'installation de MetricBeats 6.5
=========

Ce role permet d'installer et de configurer les agents Beats sur un ensemble de machines en utilisant Ansible.
Les versions Beats suivantes sont installées:

- MetricBeat
- Filebeat
- Packetbeat

Les requis
------------

Ce role requiert (sur la machine de controle):

- Ansible version > 2.0 ()
- Beats version >= 6.5
- Les machines cible ne requièrent pas d'être connectées à internet

Aucune dépendances n'est requise sur les machines où installer beats

Les os suivants ont été testés

- RedHat 7.3
- Debian 7 & 8
- Ubuntu 14.04


Role Variables
--------------

Les variables utilisées sont :

- password_kibana: Le mot de passe de l'utilisateur kibana (xpack)
- install_metricbeats : Installer MetricBeats ?
- install_filebeats : Installer FileBeats?
- application_name : Le nom de l'application à surveiller (FileBeats)
- perimetre_name : Le nom du périmètre auquel appartiennent les hosts (utilisées dans l'index)
- module_activated : Les modules à activer dans MetricBeats
- workspace : Le répertoire principale où sera installer Beats
- enable_dashboard: Activiation du dashboard dans kibana
- elastic_Output_Url : Url du serveur elasticsearch
- kibana_Output_Url : Url du serveur kibana


Dependencies
------------

- Ansible version > 2.0
- Beats version >= 6.5

Auteur
--------
`Mouhamed Cheikh Pouye`
