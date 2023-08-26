<p align="center">Laracast Servers for Laravels</p>

## About Repo 

here we going to explore how can we setup laravels server with AWS cloudformation

### Provisioning Servers on AWS

- **[ Go to AWS Cloudformation and create new stack](#)**
- **[upload stack.json file and click next and submit](#)**
- **[Once your all Recourses are created then add "EC2Instance" recourse into your stack.json](#)**
- **[update it through AWS CLI with below command, set  --stack-name with your cloudformation stack and  --template-file with stack file](#)**
- **[then you will see your instance will up and running with all configuration that you sets up in stack.json](#)**

```bash
 aws cloudformation deploy --stack-name=laracast-servers --template-file $PWD/stack.json
```

### Install PHP and nginx

After connected from ssh

```bash
 sudo apt update
 sudo apt install nginx php8.1-fpm
```
after that you can access through from  public IP (if port 80 is allowed)

```bash
 sudo apt install zip unzip php8.1-zip php8.1-curl php8.1-xml
 curl -s https://getcomposer.org/installer | php
 sudo mv composer.phar /usr/local/bin/composer
 composer --version
```
