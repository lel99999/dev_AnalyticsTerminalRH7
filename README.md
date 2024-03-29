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
- python27RH7-System ## Added to address 2.7 EOL
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

#### Launch RStudio with Flag
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

#### Google Chrome Update
To access: <br/>
`$ssh -Y <hostname> /usr/bin/google-chrome` <br/>

#### Notebook Package not installed for SCL Python3.6, R ODBC Package not included in large R Deployment

#### Update JAVA for rJAVA
```
$sudo yum install java-1.8.0-openjdk-devel
$sudo R CMD javareonf
```

#### Install rJAVA in R
```
>install.package("rJava")
```

#### Install RSQLServer DEV or STABLE through github or CRAN
```
# GITHUB
>install.packages('devtools')
>devtools::install_github('imanuelcostigan/RSQLServer')

# CRAN
>install.packages("RSQLServer")
```

<<<<<<< HEAD
#### Find what YUM packages includes a file
```
$sudo yum whatprovides "filename"
=======
#### MS ODBC Drivers for RHEL Linux
`ODBC Driver for v11.0 - libmsodbcsql-11.0.so.2270.0` <br/>

##### Add Linux Repo RHEL 7
[https://packages.microsoft.com/rhel/7/prod/](https://packages.microsoft.com/rhel/7/prod/) <br/>

```
$sudo curl https://packages.microsoft.com/config/rhel/7/prod.repo > /etc/yum.repos.d/mssql-release.repo
>>>>>>> f6fc61b0be2c4e0d76988520bd9ce602ca4b0176
```
  
  #### Install RPostgreSQL Notes
  - Requires installation of postgresql-libs and postgresql-devel
  
