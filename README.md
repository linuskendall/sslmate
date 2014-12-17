SSLMate
=========

Role for deploying certificates with SSL Mate. Automatically handles downloading of certificates as well as installs an updater to ensure that your cert is redownloaded when it is renwed. 
Assumes an existing SSLMate account as well as domains already bought on SSL Mate (via sslmate buy), see [www.sslmate.com](http://www.sslmate.com).

Requirements
------------

Should work with any of the distributions that SSL mate supports packaging for. As yet no support for source based installation (coming soon).


Role Variables
--------------

```yaml
sslmate_account_id:
sslmate_api_key:
sslmate_cert_domains:
  - domain:
    private_key
```

Example Playbook
--------------

```yaml
sslmate_account_id: 139
sslmate_api_key: {{vaulted_sslmate_api_key}}
sslmate_cert_domains:
  - domain: www.example.org
    private_key {{ lookup('file', 'keys/www.example.org.key') }}
```
