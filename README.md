```sh
    bundle install
    librarian-chef install
```

Since there is no cookbook as of writing that installs and configures Chef 11 one has to do so manually.
http://docs.opscode.com/install_server.html
```sh
   vagrant ssh chef_server
   wget https://opscode-omnibus-packages.s3.amazonaws.com/ubuntu/12.04/x86_64/chef-server_11.0.8-1.ubuntu.12.04_amd64.deb
   sudo dpkg -i chef-server_11.0.8-1.ubuntu.12.04_amd64.deb
   sudo chef-server-ctl reconfigure
```

After this is done and configured one can start doing fun stuff.