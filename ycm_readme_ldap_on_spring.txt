
This is a simple LDAP server

Configuring the server
* Primary configuration is in src/main/resources/application.properties
* LDAP Entries are configured in test-server-for-sample-web-client.ldif

Testing the server
* Option 1: visit http://localhost:8080, enter username ben and password benspassword
* Option 2: use JXplorer, enter the following details in the GUI form
  * host: localhost
  * port: 8389
  * BaseDN: dc=springframework,dc=org
  * Security level: User+Password
  * UserDN: uid=bob,ou=people,dc=springframework,dc=org
  * Password: bobspassword

Flow of Options
* Option 1
  * ChromeUser -> WebPage -> WebSecurityConfig -> LocalLdapServer
* Option 2,3
  * JXplorer -> LocalLdapServer