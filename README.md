# Vagrant VM of a Rails application with a single instance

Using ansible provisioning.

# Prepare for installing
Add ssh key to ssh-agent. It's used for code fetching from the github
```shell
ssh-add -K <path to the key> # on Mac OS
```

# Single command installing
```shell
vagrant up --provision
```

There is no autorunning for now. Therefore go to the vm and run server

```shell
vagrant ssh
cd /var/www/<project>
bundle exec rails s -b 0.0.0.0
```

open `localhost:3000` in host browser
