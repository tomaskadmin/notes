# notes

### Awesome links

https://hackr.io/

### Check internet speed via cli
````
curl -s https://raw.githubusercontent.com/sivel/speedtest-cli/master/speedtest.py | python -
````

### Configure Static IP Addresses With NetPlan (networkd)
````
# vi /etc/netplan/01-netcfg.yaml


# This file describes the network interfaces available on your system
# For more information, see netplan(5).
network:
 version: 2
 renderer: networkd
 ethernets:
   ens33:
     dhcp4: no
     dhcp6: no
     addresses: [192.168.200.201/24]
     gateway4: 192.168.200.11
     nameservers:
       addresses: [8.8.8.8,8.8.4.4]


# netplan apply
````

### git
````
# git add -A                                  - Add all files.
````

### Puppet 5 (Ubuntu 18.04)
````
# wget https://apt.puppetlabs.com/puppet5-release-bionic.deb
# dpkg -i puppet5-release-bionic.deb

# apt-get install puppetserver                - On master
# apt-get install puppet-agetn                - On slave
````
````
# puppet cert list
# puppet cert sign u18node01.lab.local
# puppet cert sign --all                      - Sign certificate requests for multiple nodes at once
# puppet agent --test
````
#### examples
````
file { 'motd':
  path    => '/etc/motd',
  content => 'Tomorrow is another day',
}
````
