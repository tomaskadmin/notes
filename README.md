# Awesome Links

https://hackr.io/

### git
````
# git add -A                                  - Add all files.
````
### KVM
````
virsh dumpxml --migratable vm01 > vm01.xml
...
virsh define vm01.xml
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
````
https://makandracards.com/makandra/1352-get-syntax-highlighting-for-puppet-files-pp-in-vi
````
#### examples
````
file { 'motd':
  path    => '/etc/motd',
  content => "Tomorrow is another day!\n",
}
````
````
# puppet resource service zabbix-agent ensure=stopped enable=false
# puppet resource package zabbix-agent ensure=purged

# puppet module list --tree
````
