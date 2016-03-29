# opendj
Ansible role for installing and configuring OpenDJ on CentOS/RHEL 6

Before using this role:

1) Download the OpenDJ ZIP package from ForgeRock Backstage: https://backstage.forgerock.com/#!/downloads/OpenDJ/OpenDJ%20Enterprise#browse
PLEASE NOTE: Review ForgeRock's license terms before using OpenDJ.

2) Copy/move the downloaded package to 'files' directory.

3) Change the 'opendj_instpkg' variable in 'defaults/main.yml' to reflect the filename of the downloaded package in 'files' directory.

4) Enter the initialization data in LDIF format into the file 'templates/initialize.ldif.j2'. Do not change the name of the file.

5) Change the 'base_dn' variable in 'defaults/main.yml' to reflect the base DN of your initialization data in 'templates/initialize.ldif.j2'.

6) Review other variables in 'defaults/main.yml' and modify as needed.

Consider using Ansible Vault instead of directly modifying the file 'defaults/main.yml' as there is some sensitive information such as passwords.

