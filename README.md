# beaker-openstack

Beaker library to use openstack hypervisor

# How to use this wizardry

This gem that allows you to use hosts with [openstack](openstack.md) hypervisor with [beaker](https://github.com/puppetlabs/beaker). 

### Right Now? (beaker 3.x)

This gem is already included as [beaker dependency](https://github.com/puppetlabs/beaker/blob/master/beaker.gemspec) for you, so you don't need to do anything special to use this gem's functionality with beaker.

### In beaker's Next Major Version? (beaker 4.x)

In beaker's next major version, the requirement for beaker-openstack will be pulled
from that repo. When that happens, then the usage pattern will change. In order
to use this then, you'll need to include beaker-openstack as a dependency right
next to beaker itself.

# Spec tests

Spec test live under the `spec` folder. There are the default rake task and therefore can run with a simple command:
```bash
bundle exec rake test:spec
```

# Acceptance tests

We run beaker's base acceptance tests with this library to see if the hypervisor is working with beaker. Please check our [openstack docs](openstack.md) to create host file to run acceptance tests. You need to set two environment variables before running acceptance tests:

1. `OPENSTACK_HOSTS` - Path to hostfile with hosts using openstack hypervisor

2. `OPENSTACK_KEY` - Path to private key that is used to SSH into Openstack VMs 

There is a simple rake task to invoke acceptance test for the library once the two environment variables are set:
```bash
bundle exec rake test:acceptance
```

# Contributing

Please refer to puppetlabs/beaker's [contributing](https://github.com/puppetlabs/beaker/blob/master/CONTRIBUTING.md) guide.
