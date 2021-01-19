Traefik (in Docker) role for Ansible
====

#### Dependencies

- docker is installed on host
- docker-compose is installed on host
- `community.general` ansible collection is installed

#### Usage

Create a playbook (`traefik.yml`) from this role:

```
---
- name: Install and configure Traefik reverse-proxy
  hosts: <your host group or individual host>
  roles:
    - role: roles/traefik
      traefik_domain: "mydomain.org"
      traefik_acme_email: "user@mydomain.org"
      traefik_dashboard_basicauth_users: ["user:$$apr1$$somehash"]
```
