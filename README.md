# Udemy Course
Docker yml for Jose Portilla's The Complete SQL Bootcamp

https://www.udemy.com/the-complete-sql-bootcamp/

## Personalize the yml file
In the yml file change these two items:

* 1. Change the postgres password to whatever you want.
```POSTGRES_PASSWORD: db_password```

* 2. Change the PGadmin Email (UN) and password to whatever you want. This is used to login to PGdmin

```PGADMIN_DEFAULT_EMAIL: email@address.com```
```PGADMIN_DEFAULT_PASSWORD: password```

## Run Docker
    1. Download and install Docker and git (Ubuntu instructions below)
        sudo apt-get install curl
        curl -fsSL get.docker.com -o get-docker.sh
        sh get-docker.sh
        sudo usermod -aG docker $(whoami)
        sudo service docker restart
        sudo -i sudo curl -L https://github.com/docker/compose/releases/download/1.21.0/docker-compose-$(uname -s)-$(uname -m) -o /usr/local/bin/docker-compose
        sudo chmod +x /usr/local/bin/docker-compose
        sudo apt-get install git
    2. Download yml file and edit it
        git clone https://github.com/tristanbolton/sqlbootcampudemy.git
        git init
        cd sqlbootcampudemy/
        nano docker-compose.yml
    3. Run docker-compose (Make sure you are in the ~/sqlbootcampudemy directory)
        sudo docker-compose up -d
    4. Done

Load PGadmin by going to http://IP_OF_UBUNTU
        

## Issues
Feel free to report any issues in https://github.com/tristanbolton/sqlbootcampudemy/issues or email help@tristanbolton.com