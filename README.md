# Development environment for Rails project in a single instance Vagrant VM

Using ansible provisioning.

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
