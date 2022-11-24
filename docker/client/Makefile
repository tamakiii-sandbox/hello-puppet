.PHONY: help

help:
	@cat $(firstword $(MAKEFILE_LIST))

setup:
	rpm -U https://yum.puppet.com/puppet7-release-el-7.noarch.rpm

install: \
	setup \
	update \
	/opt/puppetlabs/bin/puppet

update:
	yum update -y

/opt/puppetlabs/bin/puppet:
	yum install -y puppet-agent

