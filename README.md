CouchDB
=========

Install CouchDB 2.x
Quick rewrite from my Salt formula, only support standalone for the moment

Requirements
------------

CentOS

Example Playbook
--------------

```yaml
couchdb:
  repo:
    url: 'http://apache.bintray.com/couchdb-rpm/el$releasever/$basearch/'
  config:
    - section: 'chttpd'
      option: 'bind_address'
      value: '0.0.0.0'
  admin_password: admin
  users:
    - name: super
      password: man
      roles: []
    - name: zoubidou
      password: zouba
      roles: []
```

License
-------

BSD

