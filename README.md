Install Ark Survival server
=========

The role installs Ark Survival server for my server.

Role Variables
--------------

The admin password for the server should be set with ```ark_survival_admin_password```

The list of mods can be set with ```ark_survival_mods```.

The maximum number of players can be set with ```ark_survival_max_players```

The server name can be set with ```ark_survival_server_name```

The ports for the server can be set with ```ark_survival_port```, ```ark_survival_query_port``` and ```ark_survival_rcon_port```

The server can be configured to use rcon with ```ark_survival_rcon_enabled```

The user running the server can be set with ```ark_survival_name``` and ```ark_survival_group```

Example Playbook
----------------

```yaml
    - hosts: servers
      vars:
        ark_survival_admin_password: password123
        ark_survival_mods: [1609138312, 731604991, 849985437]
        ark_survival_max_players: 10
        ark_survival_server_name: "My Ark Survival Server"

      roles:
         - { role: tychobrouwer.ark_survival }

         - { role: tychobrouwer.ark_survival, ark_survival_query_port: 27015, ark_survival_rcon_enabled: true,
             ark_survival_rcon_port: 32330, ark_survival_port: 7777,
             ark_survival_name: ark, ark_survival_group: ark }

```

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
