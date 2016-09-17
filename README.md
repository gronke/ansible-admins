Ansible Role: admins
====================

Creates an admin account with a GitHub user's name and grants access for the public RSA keys. The user can use sudo to become root.

How this works
--------------

GitHub exposes every user's public keys

  https://github.com/<username>.keys

This keys are downloaded and stored with the new user's permissions in `/home/<username>/.ssh/authorized_keys`.


Example
-------
Configure administrator access for @gronke
```yaml
- role: gronke.admins
  GITHUB_USER: gronke  
```
 
