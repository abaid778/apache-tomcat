# apache-tomcat

### tomcat apache Installation on Ubuntu 14.04
* `sudo apt-get update`
* `sudo apt-get install tomcat7`
* `sudo service tomcat7 restart`

http://server_IP_address:8080
* `sudo apt-get install tomcat7-docs tomcat7-admin tomcat7-examples`
* `sudo apt-get install default-jdk`
* `sudo apt-get install ant git`

Open file `/etc/tomcat7/tomcat-users.xml`
add this 

`<tomcat-users>`
`<user username="admin" password="password" roles="manager-gui,admin-gui"/>`
`</tomcat-users>`

* `sudo service tomcat7 restart`
Now open browser `http://server_IP_address:8080/manager/html`

Now change the port to 80 

open the file `/etc/tomcat7/server.xml`

* `apt-get install authbind`

First, set `AUTHBIND=yes` in `/etc/default/tomcat7` file

* `sudo touch /etc/authbind/byport/80`
* `sudo chmod 500 /etc/authbind/byport/80`
* `sudo chown tomcat7 /etc/authbind/byport/80`
* `sudo service tomcat7 restart`
