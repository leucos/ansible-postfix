Ansible Postfix role
====================

This role installs Postfix.

It is very basic, just cover my needs. PRs welcomed.

Variables
---------

Most of them are self-explanatory.

- `postfix_smtpd_tls_cert_file`: TLS certificate file (default: /etc/ssl/certs/ssl-cert-snakeoil.pem)
- `postfix_smtpd_tls_key_file`: TLS key file (default: /etc/ssl/private/)ssl-cert-snakeoil.key
- `postfix_smtpd_use_tls`: Use TLS or not (default: "yes")
- `postfix_inet_interfaces`: IP to listen on (default: [ "all" ])
- `postfix_mydestination`: Destination domains/hostnames (default: [])
- `postfix_mynetworks`: Allowed networks for non local destinations (default: [])
- `postfix_relayhost`: SMTP relay host (default: "")
- `postfix_virtual_alias_maps`: Virtual alias maps (default: False)
- `postfix_virtual_mailbox_domains`: Virtual domains (default: False)
- `postfix_virtual_mailbox_maps`: Virtual mailbox maps (default: False)
- `postfix_virtual_mailbox_base`: Virtual mailbox base (default: False)
- `postfix_virtual_minimum_uid`: Minimum UID (default: False)
- `postfix_virtual_transport`: Virtual transport (default: False, which leads to the postfix default "virtual")
- `postfix_virtual_uid_maps`: UID maps (default: False)
- `postfix_virtual_gid_maps`: GID maps (default: False)

Tests
-----

Test can then be run using vagrant:

```
vagrant up
vagrant ssh -c specs
```

Licence
-------

MIT
