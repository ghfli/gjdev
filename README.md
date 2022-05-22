# gjdev
gym-jinni playground
 
Set up the development VM with
[Vagrant](https://www.vagrantup.com/docs/providers/configuration). Tested
libvirt as the provider for setting up an archlinux VM on an archlinux host.
See more details in the Vagrantfile and setup-alx.sh. Remember to install
nfs-utils on the host to make sure the /vagrant mounted on the VM by default
can be synced bidirectionally to and from the current working directory.

Test [flutter](https://docs.flutter.dev/reference/tutorials) +
[hereoku](https://devcenter.heroku.com/categories/heroku-architecture)
([go](https://devcenter.heroku.com/categories/go-support) +
[postgres](https://devcenter.heroku.com/categories/heroku-postgres))

On the host:

    vagrant up  # bring up the VM
    vagrant ssh # login to the VM

On the VM:

    cd /vagrant
    flutter create hello_flutter
    cd hello_flutter
    flutter build web
    darkhttpd build/web

Point the browser to http://localhost:8080 on the host.
