# automysqlbackup
A fork and fix of AutoMySQLBackup for our standard installations.

AutoMySQLBackkup has been modified to support newer versions of MySQL

* support for MySQL 5.6 and 5.7
* login path support (no passwords required on the command line)
* fixed --ssl paramter usage in 5.7+

Modern usage includes the login path support so that credentials are not required
on the command line when calling mysqldump (etc).

As root, create the credentials for logging into MySQL

 mysql_config_editor set --login-path=automysqldump --user=root -p

The automysqlbackup.conf file is configured to look for the login path "automysqldump" 
credentials in the ".mylogin.conf" file in folder "/root"

