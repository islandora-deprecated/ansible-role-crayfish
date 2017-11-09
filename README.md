# Ansible Role: Crayfish

An Ansible role that installs [Crayfish](https://github.com/Islandora-CLAW/Crayfish) on:

* Centos/RHEL 7.x
* Ubuntu Xenial

## Role Variables

Available variables are listed below, along with default values:

User to use when installing webservices:
```
crayfish_user: www-data
```

Version to install:
```
crayfish_version_tag: 0.0.7
```

Services to install:
```
crayfish_services:
  - Gemini
  - Houdini
  - Milliner
  - Hypercube
```

Static JWT token to add:
```
crayfish_syn_token: islandora
```

There are lots more configuration settings in [defaults/main.yml](defaults/main.yml)

## Dependencies

* Apache webserver
* PHP 7
  
## Example Playbook

    - hosts: webservers
      roles:
        - { role: islandora.crayfish }

## License

MIT