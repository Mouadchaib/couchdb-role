# Ansible Role: CouchDB

[![Build Status](https://travis-ci.org/personnage/ansible-role-couchdb.svg?branch=master)](https://travis-ci.org/personnage/ansible-role-couchdb)

Installs CouchDB on Debian/Ubuntu servers.

## Requirements

None

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    couchdb_port: "5984"
    couchdb_bind_address: "127.0.0.1"
    couchdb_database_dir: "/var/lib/couchdb"
    couchdb_view_index_dir: "/var/lib/couchdb"
    couchdb_max_dbs_open: 100
    couchdb_delayed_commits: true
    couchdb_log_level: "info"

## Dependencies

None

## Example Playbook

    - hosts: webservers
      vars:
        couchdb_max_dbs_open: 150
      roles:
        - { role: personnage.couchdb }
