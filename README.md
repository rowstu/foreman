# foreman install

Very quick start to get a Foreman server up and running under RHEL8
```
sudo firewall-cmd --add-service http --permanent
sudo firewall-cmd --add-service https --permanent
sudo firewall-cmd --add-port 8443/tcp --permanent
sudo firewall-cmd --add-port 8140/tcp --permanent
sudo dnf -y install https://yum.puppet.com/puppet7-release-el-8.noarch.rpm
sudo dnf -y install https://yum.theforeman.org/releases/3.7/el8/x86_64/foreman-release.rpm
sudo dnf module enable foreman:el8
sudo dnf -y install foreman-installer
sudo foreman-installer
```
