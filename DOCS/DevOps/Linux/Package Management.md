### RPM (Redhat Package Manager)

``` bash
rpm -i package_to_install.rpm
```

``` bash
rpm -e package_to_uninstall.rpm
```

``` bash
rpm -q package_to_query.rpm
```


### YUM( Uses RPM under the hood)

* Uses /etc/yum.repos.d to query remote repositories to get other dependencies needed to install any package.

``` bash
yum install ansible
```

``` bash
yum remove ansible
```

