# Coding challenge II: Save our deploy train
 
In this coding challenge, we used ansible and docker-compose to deploy these two containers: **PHP and Nginx**.

### Objective:

We have created three vhosts in nginx to enable developers to test their code without training traffic jams.

## Prerequisite:

we need to have installed:

- ansible
- docker
- docker-compose

## Configure Host File

we need to modify the hosts file:

1. Open the host file in a text edior:

```sh
vim /etc/hosts
```
2. Add the following three lines:

```sh
127.0.0.1       test1.testycan.shop
127.0.0.1       test2.testycan.shop
127.0.0.1       test3.testycan.shop
```

3. Save and exit the file.


##  Runing the envirenoment 

To deploy our application by launching our playbook with the following command:

```sh
ansible-playbook -i 00_inventory.yml  playbook.yml 
```
