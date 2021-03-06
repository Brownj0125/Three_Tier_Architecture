Cloud-Student
Full Sail Course Account

These files are for class projects and not for production use.

Any IPs, usernames, passwords, keys, and secrets found are fake and for demonstration/class purposes only.

This is a three tier architecture

Tier 1 MariaDB
Tier 2 SeedDMS
Tier 3 Load Balancer

--- Order of Events ----
UPDATE hosts file with public ip addresses of instances.
MariaDB.yml - Database must be first.
EDIT File/settings.xml - Line 101:  Change dbHostname IP, dbDatabase name, dbUser name, and dbPass password to reflect the database configurations.
SeedDMSInitialDB.yml - Run this on the on the first instance go to http://<Public_IP>/install/install.php initialize the Database.
SeeddmsIniCleanup.yml - Run IF the delete of ENABLE_INSTALL_TOOL fails.
SeeddmsPool.yml - Run on all other instances.
EDIT File/haproxy.cfg file for web server private address.
HAproxy.yml - Configures the load balancer.
