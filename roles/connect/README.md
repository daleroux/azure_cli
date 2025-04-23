Daleroux.Azure_cli Connect Role
========================

Role which allows to connect to Azure cli with credentials and then installs the graph module

Requirements
------------

Role Variables
--------------

spn_client_id: Service Principal Client ID
spn_secret:    Service Principal Secret
tenant_id:     Tenant ID

Dependencies
------------

N/A

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```yaml
- name: Execute tasks on servers
  hosts: servers
  roles:
    - role: daleroux.azure_cli.connect
      
```

Another way to consume this role would be:

```yaml
- name: Initialize the connect role from daleroux.azure_cli
  hosts: servers
  gather_facts: false
  tasks:
    - name: Trigger invocation of connect role
      ansible.builtin.include_role:
        name: daleroux.azure_cli.connect
      vars:
        spn_client_id: Some client ID
        spn_secret:    #preferably vaulted var
        tenant_id:     Some Tenant ID
```

License
-------

# TO-DO: Update the license to the one you want to use (delete this line after setting the license)
BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
