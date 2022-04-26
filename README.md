## Configure IP address of Ubuntu Server by using Netplan method

### Software Used
| Software      | Version                 |
| -----------   | -----------             |
| VirtualBox    | VirtualBox 6.1          |
| Ubuntu Server | Ubuntu Server 20.04 LTS |

- Configuration file (00-installer-config.yaml)
~~~
sudo vim /etc/netplan/00-installer-config.yaml
sudo netplan apply
~~~

- Options to configure **00-installer-config.yaml** file

> Static IP configuration
~~~
network:
    ethernets:
        enp0s3:
            addresses: [192.168.0.1/24]
        version: 2
~~~

> Automatic (DHCP) IP configuration
~~~
network:
    ethernets:
        enp0s3:
            dhcp4: true
        version: 2
~~~
