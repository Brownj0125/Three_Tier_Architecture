<h1>IT Technology-Student<br>
Full Sail University: Course Account</h1>

These files are for class projects and not for production use.<br>
Use at your own risk.<br>
Any IPs, usernames, passwords, keys, and secrets found are fake and for demonstration/class purposes only.<br>

<h2>This course is about setting up a three tier architecture</h2>

<h3>Tier 1 CentOS - MariaDB: SQL<br>
Tier 2 CentOS - SeedDMS: Web App<br>
Tier 3 Ubuntu - HAProxy: Load Balancer<br></h3>

--- Order of Events ----<br>
1. Install Ansible on host.<br>
2. Create VM and all dependencies add a public-ip.<br>
3. Clone repository to Ansible host.<br>
4. UPDATE hosts file with public ip addresses of instances.<br>
5. MariaDB.yml - Database must be first.<br>
6. EDIT File/settings.xml - Line 101:  Change dbHostname IP, dbDatabase name, dbUser name, and dbPass password to reflect the database configurations.<br>
7. SeedDMSInitialDB.yml - Run this on the on the first instance go to http://<Public_IP>/install/install.php initialize the Database.<br>
8. SeeddmsIniCleanup.yml - Run IF the delete of ENABLE_INSTALL_TOOL fails.<br>
9. SeeddmsPool.yml - Run on all other instances.<br>
10. EDIT File/haproxy.cfg file for web server private address.<br>
11. HAproxy.yml - Configures the load balancer.
