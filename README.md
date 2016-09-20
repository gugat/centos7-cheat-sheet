# Centos 7 Cheat Sheet

## General

Update system

    yum update

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


