# Centos 7 Cheat Sheet

## General

Update system

    yum update

## Main utilities

    yum install wget
    
## Network

Network configuration
    
    nmtui

List network connections
    
    nmcli d


Show ip address if you know the device name (e.g eth0)
    
    ip addr show eth0
    
Show ip address if you don't know the device name

    ip route show

Restart network service

    systemctl restart network

## Mysql

_Based on [Linode's installation guide](https://www.linode.com/docs/databases/mysql/how-to-install-mysql-on-centos-7)_

Install mysql 

    yum update
    wget http://repo.mysql.com/mysql-community-release-el7-5.noarch.rpm
    sudo rpm -ivh mysql-community-release-el7-5.noarch.rpm
    yum update
    sudo yum install mysql-server

Start mysql service

    systemctl start mysqld

Root login

     mysql -u root -p


Create user
    
    create user 'testuser'@'localhost' identified by 'password';

Create database

    create database testdb;

Grant permissions

    grant all on testdb.* to 'testuser' identified by 'password';
