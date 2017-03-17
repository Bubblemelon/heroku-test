# heroku-test
Exploring Heroku

### Reference:
https://devcenter.heroku.com/articles/getting-started-with-php

https://github.com/heroku/php-getting-started 

### Installing Heroku Commandline Interface:


```
# Run this from your terminal.
# Replace OS with one of “linux”, “darwin”, “windows”, “freebsd”, “openbsd”
# Replace ARCH with one of “amd64”, “386” or “arm”
#Example: tar -xvzf heroku-OS-ARCH.tar.gz -C /usr/local/lib
# ensure that /usr/local/bin is in the PATH environment variable 

wget https://cli-assets.heroku.com/branches/stable/heroku-OS-ARCH.tar.gz

mkdir -p /usr/local/lib /usr/local/bin

tar -xvzf heroku-lix-amd64.tar.gz -C /usr/local/lib

ln -s /usr/local/lib/heroku/bin/heroku /usr/local/bin/heroku
```

### Installing Composer

_To use outside of project folder:_

```
curl -sS https://getcomposer.org/installer | sudo php -- --install-dir=/usr/local/bin --filename=composer

# Taken from: https://www.digitalocean.com/community/tutorials/how-to-install-and-use-composer-on-ubuntu-14-04 
```

XOR

```
php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"

php -r "if (hash_file('SHA384', 'composer-setup.php') === '669656bab3166a7aff8a7506b8cb2d1c292f042046c5a994c43155c0be6190fa0355160742ab2e1c88d40d5be660b410') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"

sudo php composer-setup.php --install-dir=/usr/local/bin --filename=composer

php -r "unlink('composer-setup.php');"

# Taken from: https://getcomposer.org/download/

```

_To use within project folder:_

Download composer using the DigitalOcean method or use the getcomposer instructions by placing folder location.

XOR

`cd` into project folder and download composer without needing to place folder location.  

### Heroku Apps

A Free account limits up to 5 apps.

_Type into terminal to delete all apps:_

``` 
for app in $(heroku apps); do heroku apps:destroy --app $app --confirm $app; done 
```
_To Manualy Delete individual apps:_

https://dashboard.heroku.com/apps/

### Deployed Example

https://aqueous-atoll-17679.herokuapp.com/  [may not be active]


### How to add Submodules can be found here:

https://github.com/blog/2104-working-with-submodules

The link above explains/clarifies the question found in: http://stackoverflow.com/questions/14448601/what-does-this-green-icon-mean-in-a-github-repository

This is in reference to my experience when adding the heroku remote repository into my "heroku-test"repository.



