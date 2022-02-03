keycloak
========

[![Build Status](https://travis-ci.org/andrelohmann/ansible-role-keycloak.svg?branch=master)](https://travis-ci.org/andrelohmann/ansible-role-keycloak)

Use this role to install keycloak.

Requirements
------------

This role requires Redhat Enterprise Linux 8.

Keycloak 16.1.0 shall be placed under */data/keycloak* directory.

Dependencies
------------



Role Variables
--------------

The default set of variables defines the settings, keycloak will be installed with

    keycloak_version: 16.1.0
    keycloak_dir: /data/keycloak
    keycloak_archive: keycloak-{{ keycloak_version }}.tar.gz
    keycloak_url: http://downloads.jboss.org/keycloak/{{ keycloak_version }}/{{keycloak_archive }}
    keycloak_jboss_home: "{{ keycloak_dir }}/keycloak-{{ keycloak_version }}"
    keycloak_log_dir: "{{ keycloak_jboss_home }}/standalone/log"
    keycloak_bind_port: "8080"
    keycloak_bind_address: "0.0.0.0"
    keycloak_admin_username: "admin"
    keycloak_admin_password: "admin"
    keycloak_create_admin: True

Example Playbook
----------------

    - hosts: keycloak
      roles:
         - andrelohmann.keycloak

License
-------

MIT

Original Author Information
------------------

https://github.com/andrelohmann
