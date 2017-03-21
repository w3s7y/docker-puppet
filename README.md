# Puppet in a container.
Could be good for anyone wanting to write/test puppet code but are
worried about it destroying their machine!  
This way they can run puppet code in an isolated container,
check the output and then adjust and rerun.


## Use
To use this, have your puppet directory
(/etc/puppetlabs/code/environments/production) ready on the host machine.
With all of the modules and a manifest ready to go.

### Interactive run (logs goto stdout).
```shell
docker run -i -v <path to your puppet code>:/etc/puppetlabs/code/environments/production benwest/puppet
```
