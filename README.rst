

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
