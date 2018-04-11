Role Name
=========

A quick role to configure Apache as a reverse proxy that requires LDAP based authentication.  Useful for restricting access to a webservice that doesn't natively know how to authenticate against LDAP. In this case it's used with Kibana to put some basic access controls in place.

Notes
-----
This assumes many things about a base CentOS 7 Apache 2.4 install

Role Variables
--------------

* apache_auth_name - Title of the authentication prompt
* apache_ldap_url - URL and search domain for Apache to use when connecting to LDAP
* apache_ldap_bind_dn - LDAP DN with suitable permissions
* apache_ldap_bind_password - suitable bind password for searching
* apache_proxy_dest - where proxied traffic is directed, usually this is Kibana on the loopback adapter
* apache_proxy_user_username - Overrides the browser provided username
* apache_proxy_user_password - Overrides the browser provided password
* apache_ldap_ssl_{crt,ca,key} - TLS cert files for apache
* apache_ldap_ssl_{crt,ca,key}_dest - Where the cert files are stored
=======
# apache_auth-role
LDAP Authenticating Apache Proxy
