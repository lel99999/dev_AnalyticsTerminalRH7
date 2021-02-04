# dev_AnalyticsTerminalRH7
Development of Analytics Terminal for RHEL 7

# Update Roles
- devtools -> devtools7 
- clouseau
- common7
- epel7
- intellij
- iptables
- jdk -> openjdk1.8
- maven
- nginx
- nodejs -> v8, v10 via SCL 
- odbc -> odbc7
- postgresql-client -> postgresql-client7
- pycharm
- pyenvRH7
- python-libs
- python2RH7
- python3RH7
- r-shiny-configRH7
- r-shinyRH7
- r-studio-desktopRH7
- r-studio-server-configRH7
- r-studio-serverRH7
- r_RH7
- redis2 -> redis5
- ruby
- shared7
- spark2 -> spark3
- sublime2 -> sublime3
- stattransfer14

#### Ansible SSH Connection Error
Add following in /etc/ansible/hosts <ip> <hostname> ansible_ssh_pass=vagrant ansible_ssh_user=vagrant  <br/>

#### Remove Postgres 9.4 REPO Error, No longer Exists/Supported
