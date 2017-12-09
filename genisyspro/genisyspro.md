GenisysPro Template

Before using you'll need to install the following

```
##Ubuntu/Debian
sudo apt install libltdl7 unzip
```
```
##CentOS
sudo yum install libltdl7 unzip
```

You can install this template by running

```bash
curl -o /var/lib/pufferd/templates/genisyspro.json https://paste.ee/r/4BBcl/0 && chown pufferd:pufferd /var/lib/pufferd/templates/genisyspro.json
```

Note: The install guide for GenisysPro requires you to edit `GenisysPro-master/bin/php7/bin/php.ini` with the full path to opcache.so

So for example, mine looks like
```bash
zend_extension=/var/lib/pufferd/servers/6e0a6050-b1f8-451d-84b4-8aa01a77d94b/GenisysPro-master/bin/php7/lib/php/extensions/no-debug-zts-20151012/opcache.so
```

However, it does appear to run without making this change.
