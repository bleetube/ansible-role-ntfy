# Ansible Role: ntfy

Recommended alternative: [stevenengland/ntfy_ansible_role](https://github.com/stevenengland/ntfy_ansible_role)

This Ansible Role installs binwiederhier's [ntfy](https://github.com/binwiederhier/ntfy).

Related role: [ansible-role-ntfy-alertmanager](https://github.com/bleetube/ansible-role-ntfy-alertmanager) for xenrox's ntfy-alertmanager integration.

## Requirements

None.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

```yaml
ntfy_base_url: http://ntfy.example.com
ntfy_listen_http: ":80"
```

For more configuration info, see the upstream [configuration docs](https://docs.ntfy.sh/config/).

## Example Playbook

```yaml
- hosts: all
  roles:
    - role: bleetube.ntfy
      become: true
```

## Resources

* binwiederhier publishes the [configuration for his production server](https://github.com/binwiederhier/ntfy-ansible/blob/main/roles/ntfy/templates/server.yml.j2) in an Ansible playbook.