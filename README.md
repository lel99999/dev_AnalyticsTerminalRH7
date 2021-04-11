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
- r-shinyRH7 -> v1.5.16.958
- r-studio-desktopRH7 -> v1.14.1106
- r-studio-server-configRH7
- r-studio-serverRH7 -> v.1.14.1106
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

#### Python Pip for RHEL 7
[https://access.redhat.com/solutions/1519803](https://access.redhat.com/solutions/1519803) <br/>

#### Shiny Server Issues
- [Shiny Server Service Issue](https://github.com/rstudio/shiny-server/issues/316)

#### Launch RStudio
```
$ssh -Y <host> QMLSCENE_DEVICE=software rstudio
```

#### Modified/Removed Packages
- Postgresql 9.x
- Postgis24-9x

#### Updated/Added Packages
- Postgis25-10*
- Python27 System Role


#### Python 2.7 Pip Error Fix
Error: <br/>
```
$scl enable python27 bash
$pip
Traceback (most recent call last):
  File "/opt/rh/python27/root/usr/bin/pip", line 7, in <module>
    from pip._internal.cli.main import main
  File "/opt/rh/python27/root/usr/lib/python2.7/site-packages/pip/_internal/cli/main.py", line 60
    sys.stderr.write(f"ERROR: {exc}")
                                   ^
SyntaxError: invalid syntax
```
Fix: <br/>
```
$curl -O https://bootstrap.pypa.io/pip/2.7/get-pip.py
$python get-pip.py
$python -m pip install --upgrade "pip < 21.0"
```
#### Addressing YAML Errors:
Use yamllint: <br/>
```
$brew install yamllint
$yamllint <yaml_file>
```
![yamllint results](https://github.com/lel99999/dev_AnalyticsTerminalRH7/blob/master/yamllint-01.png) <br/>

[Quickstart](https://yamllint.readthedocs.io/en/stable/quickstart.html) <br/>

