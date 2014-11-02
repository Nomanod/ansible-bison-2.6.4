Bison
=========

Compile specific version of Bison

Point to consider
-----------------

I don't have any bison installed on the system.

I thought off this role to install any version of bison, but i saw
that in git repository there are some missing files. Therefore, i
extracted these files from compressed tar.gz[1]. You can see this in
the task "Copying missing files to the repository"

[1]https://gist.github.com/krahser/b11b23fb39fd5328b440

Other references:
- Publication of compressed file
http://savannah.gnu.org/forum/forum.php?forum_id=7406
- Git Browser repository
http://git.savannah.gnu.org/cgit/bison.git

If you are compiling a different version, then make sure you use the
right files.

Role Variables
--------------

- bison_path:: Set the path to copy the repository
- bison_tag:: Set the version to compile


Example Playbook
----------------


	- name: compile bison
	  hosts: Ansible
	  roles:
	  - { role: krahser.bison}

License
-------

GPLv3

