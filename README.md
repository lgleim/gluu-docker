<p align="center"><img src="https://www.gluu.org/wp-content/themes/gluu/images/gl.png"></p>

# Gluu C.E Docker
Altough Gluu has officialy Docker Edition Workflows it is too complex and has many requirements.  

# Quick Start
Create an empry directory and inside that:

```bash
# Clone repo
git clone https://github.com/pi0/gluu-docker sso
cd sso

# Edit env file
[ ! -f env ] && cp -rv env.example env
$EDITOR env 

# Setup
docker-compose run --rm ldap setup

# Compose up!
docker-compose up -d

# View default password
cat data/gluu_install/setup.properties|grep ldapPass=
```
