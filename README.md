# Ansible-TD

## Installation

Pour installer Ansible sur votre machine : [https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html)

`git clone https://github.com/Thorin10/Ansible-TD.git`


## Modification
* Dans le fichier **ansible.cfg** modifier `private_key_file` par votre clée privée ssh

* Dans le dossier `/host_vars/`
 	* [X] **ansible_host:**  IP public des machines

* Dans `/ansible.cfg` & `/playbook/playbook.yml`
	 - [X] `remote_user` = **le nom de votre utilisateur des machines**.
 
* Dans `/playbook/roles/mysql/tasks/main.yml` 
	* **Create wordpress user** 
		 * [x] `host` =  l'ip **privé** de votre VM Database.

* Dans `/playbook/roles/wordpress/defaults/main.yml`
	 * [x] IP `wp_db_host`
	 * [x] IP Privé `VM Wordpress`

## Lancement

Pour lancer l'installation par les playbooks utilisez:

    `ansible-playbook playbooks/playbook.yml -i ./host.ini`

---

**Vous avez donc maintenant accès à Wordpress depuis votre VM Apache avec l'IP public de cette dernière**


