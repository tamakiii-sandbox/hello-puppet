.PHONY: help setup install update
.PHONY: version

help:
	@cat $(firstword $(MAKEFILE_LIST))

version:
	/opt/puppetlabs/bin/puppetserver --version

setup:
	rpm -U https://yum.puppet.com/puppet7-release-el-7.noarch.rpm

install: \
	setup \
	update \
	/opt/puppetlabs/bin/puppet \
	/opt/puppetlabs/bin/puppetserver

update:
	yum update -y

/opt/puppetlabs/bin/puppet:
	yum install -y puppet

/opt/puppetlabs/bin/puppetserver:
	yum install -y puppetserver

