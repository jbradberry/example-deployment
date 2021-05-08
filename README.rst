

Notes
-----

The ansible.cfg file is intended to support the case of devs running
Ansible commands manually, locally, in an environment where they may
be working on multiple projects each with their own separate (and
potentially incompatible) requirements.  It specifies role and
collection paths local to the project, but doing so means that they
have to be installed using two commands:

.. code-block:: bash

   $ ansible-galaxy role install -r requirements.yml
   $ ansible-galaxy collection install -r requirements.yml

The ansible.cfg should be left off if using e.g. the Ansible
Automation Platform.


TODO
----

- Ensure that the proposed environments structure can be imported into
  Ansible Tower with a minimum of pain, especially encrypted Vault
  files.  See:
  `<https://docs.ansible.com/ansible-tower/latest/html/administration/tipsandtricks.html#importing-existing-inventory-files-and-host-group-vars-into-tower>`_

- Replace the concept of playbooks/group_vars/* with explicitly
  included var files.  Ansible commands other than
  ``ansible-playbook`` do not respect playbooks/group_vars/ files.
  See:
  `<https://docs.ansible.com/ansible/latest/user_guide/intro_inventory.html#organizing-host-and-group-variables>`_
