Role Name
=========

Role for installing the legacy Fedore Commons 3 repository in an existing tomcat. 
Requirements
------------

1. Tomcat

Role Variables
--------------
```yaml

# Version of Fedora to install. Only tested with 3.8.1
fedora_version: 3.8.1

#Where to Install Fedora
fedora_install_dir: /opt/fedora
catalina_home: /var/lib/tomcat

# Downloads  binaries to a local directory on the host machine to avoid repeated downloads
downloads_directory: /opt/downloads

fedora_port: 8080

fedora_admin_password: password

fedora_pid_namespace: changeme

fedora_oai_max_records: 500
fedora_oai_max_headers: 500
fedora_admin_emails: []
fedora_repository_name: A Fedora Repository
fedora_repository_domain: example.edu

```



Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: ansible-fcrepo3-role, fedora_repository_name: "Ben's Magical Tinderbox of Chinlint" }

License
-------

BSD

Author Information
------------------

Temple University Library Developers
