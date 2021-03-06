---
layout: default
title: "Indirection Reference"
canonical: "/references/latest/indirection.html"
---


# Indirection Reference



**This page is autogenerated; any changes will get overwritten** *(last generated on Tue Aug 21 17:55:38 -0700 2012)*

This is the list of all indirections, their associated terminus classes, and how you select between them.

In general, the appropriate terminus class is selected by the application for you (e.g., `puppet agent` would always use the `rest`
terminus for most of its indirected classes), but some classes are tunable via normal settings.  These will have `terminus setting` documentation listed with them.


## catalog

* **Terminus Setting**: catalog_terminus

active_record
: (undocumented)

active_record
: (undocumented)

compiler
: Puppet's catalog compilation interface, and its back-end is
  Puppet's compiler

compiler
: Puppet's catalog compilation interface, and its back-end is
  Puppet's compiler

queue
: (undocumented)

queue
: (undocumented)

rest
: Find resource catalogs over HTTP via REST.

rest
: Find resource catalogs over HTTP via REST.

static_compiler
: (undocumented)

static_compiler
: (undocumented)

store_configs
: (undocumented)

store_configs
: (undocumented)

yaml
: Store catalogs as flat files, serialized using YAML.

yaml
: Store catalogs as flat files, serialized using YAML.

## certificate



ca
: Manage the CA collection of signed SSL certificates on disk.

ca
: Manage the CA collection of signed SSL certificates on disk.

file
: Manage SSL certificates on disk.

file
: Manage SSL certificates on disk.

rest
: Find and save certificates over HTTP via REST.

rest
: Find and save certificates over HTTP via REST.

## certificate_request



ca
: Manage the CA collection of certificate requests on disk.

ca
: Manage the CA collection of certificate requests on disk.

file
: Manage the collection of certificate requests on disk.

file
: Manage the collection of certificate requests on disk.

rest
: Find and save certificate requests over HTTP via REST.

rest
: Find and save certificate requests over HTTP via REST.

## certificate_revocation_list



ca
: Manage the CA collection of certificate requests on disk.

ca
: Manage the CA collection of certificate requests on disk.

file
: Manage the global certificate revocation list.

file
: Manage the global certificate revocation list.

rest
: Find and save certificate revocation lists over HTTP via REST.

rest
: Find and save certificate revocation lists over HTTP via REST.

## certificate_status



file
: (undocumented)

file
: (undocumented)

rest
: Sign, revoke, search for, or clean certificates & certificate requests over HTTP.

rest
: Sign, revoke, search for, or clean certificates & certificate requests over HTTP.

## facts

* **Terminus Setting**: facts_terminus

active_record
: (undocumented)

active_record
: (undocumented)

couch
: (undocumented)

couch
: (undocumented)

facter
: Retrieve facts from Facter.  This provides a somewhat abstract interface
  between Puppet and Facter.  It's only `somewhat` abstract because it always
  returns the local host's facts, regardless of what you attempt to find.

facter
: Retrieve facts from Facter.  This provides a somewhat abstract interface
  between Puppet and Facter.  It's only `somewhat` abstract because it always
  returns the local host's facts, regardless of what you attempt to find.

inventory_active_record
: (undocumented)

inventory_active_record
: (undocumented)

inventory_service
: Find and save facts about nodes using a remote inventory service.

inventory_service
: Find and save facts about nodes using a remote inventory service.

memory
: Keep track of facts in memory but nowhere else.  This is used for
  one-time compiles, such as what the stand-alone `puppet` does.
  To use this terminus, you must load it with the data you want it
  to contain.

memory
: Keep track of facts in memory but nowhere else.  This is used for
  one-time compiles, such as what the stand-alone `puppet` does.
  To use this terminus, you must load it with the data you want it
  to contain.

network_device
: Retrieve facts from a network device.

network_device
: Retrieve facts from a network device.

rest
: Find and save facts about nodes over HTTP via REST.

rest
: Find and save facts about nodes over HTTP via REST.

store_configs
: (undocumented)

store_configs
: (undocumented)

yaml
: Store client facts as flat files, serialized using YAML, or
  return deserialized facts from disk.

yaml
: Store client facts as flat files, serialized using YAML, or
  return deserialized facts from disk.

## file_bucket_file



file
: Store files in a directory set based on their checksums.

file
: Store files in a directory set based on their checksums.

rest
: This is a REST based mechanism to send/retrieve file to/from the filebucket

rest
: This is a REST based mechanism to send/retrieve file to/from the filebucket

selector
: Select the terminus based on the request

selector
: Select the terminus based on the request

## file_content



file
: Retrieve file contents from disk.

file
: Retrieve file contents from disk.

file_server
: Retrieve file contents using Puppet's fileserver.

file_server
: Retrieve file contents using Puppet's fileserver.

rest
: Retrieve file contents via a REST HTTP interface.

rest
: Retrieve file contents via a REST HTTP interface.

selector
: Select the terminus based on the request

selector
: Select the terminus based on the request

## file_metadata



file
: Retrieve file metadata directly from the local filesystem.

file
: Retrieve file metadata directly from the local filesystem.

file_server
: Retrieve file metadata using Puppet's fileserver.

file_server
: Retrieve file metadata using Puppet's fileserver.

rest
: Retrieve file metadata via a REST HTTP interface.

rest
: Retrieve file metadata via a REST HTTP interface.

selector
: Select the terminus based on the request

selector
: Select the terminus based on the request

## instrumentation_data



local
: (undocumented)

local
: (undocumented)

rest
: (undocumented)

rest
: (undocumented)

## instrumentation_listener



local
: (undocumented)

local
: (undocumented)

rest
: (undocumented)

rest
: (undocumented)

## instrumentation_probe



local
: (undocumented)

local
: (undocumented)

rest
: (undocumented)

rest
: (undocumented)

## inventory

* **Terminus Setting**: inventory_terminus

yaml
: Return node names matching the fact query

yaml
: Return node names matching the fact query

## key



ca
: Manage the CA's private on disk.  This terminus *only* works
  with the CA key, because that's the only key that the CA ever interacts
  with.

ca
: Manage the CA's private on disk.  This terminus *only* works
  with the CA key, because that's the only key that the CA ever interacts
  with.

file
: Manage SSL private and public keys on disk.

file
: Manage SSL private and public keys on disk.

## node

Where to find node information.
A node is composed of its name, its facts, and its environment.

* **Terminus Setting**: node_terminus

active_record
: (undocumented)

active_record
: (undocumented)

exec
: Call an external program to get node information.  See
  the [External Nodes](http://docs.puppetlabs.com/guides/external_nodes.html) page for more information.

exec
: Call an external program to get node information.  See
  the [External Nodes](http://docs.puppetlabs.com/guides/external_nodes.html) page for more information.

ldap
: Search in LDAP for node configuration information.  See
  the [LDAP Nodes](http://projects.puppetlabs.com/projects/puppet/wiki/Ldap_Nodes) page for more information.  This will first
  search for whatever the certificate name is, then (if that name
  contains a `.`) for the short name, then `default`.

ldap
: Search in LDAP for node configuration information.  See
  the [LDAP Nodes](http://projects.puppetlabs.com/projects/puppet/wiki/Ldap_Nodes) page for more information.  This will first
  search for whatever the certificate name is, then (if that name
  contains a `.`) for the short name, then `default`.

memory
: Keep track of nodes in memory but nowhere else.  This is used for
  one-time compiles, such as what the stand-alone `puppet` does.
  To use this terminus, you must load it with the data you want it
  to contain; it is only useful for developers and should generally not
  be chosen by a normal user.

memory
: Keep track of nodes in memory but nowhere else.  This is used for
  one-time compiles, such as what the stand-alone `puppet` does.
  To use this terminus, you must load it with the data you want it
  to contain; it is only useful for developers and should generally not
  be chosen by a normal user.

plain
: Always return an empty node object. Assumes you keep track of nodes
  in flat file manifests.  You should use it when you don't have some other,
  functional source you want to use, as the compiler will not work without a
  valid node terminus.

  Note that class is responsible for merging the node's facts into the
  node instance before it is returned.

plain
: Always return an empty node object. Assumes you keep track of nodes
  in flat file manifests.  You should use it when you don't have some other,
  functional source you want to use, as the compiler will not work without a
  valid node terminus.

  Note that class is responsible for merging the node's facts into the
  node instance before it is returned.

rest
: This will eventually be a REST-based mechanism for finding nodes.  It is currently non-functional.

rest
: This will eventually be a REST-based mechanism for finding nodes.  It is currently non-functional.

store_configs
: (undocumented)

store_configs
: (undocumented)

yaml
: Store node information as flat files, serialized using YAML,
  or deserialize stored YAML nodes.

yaml
: Store node information as flat files, serialized using YAML,
  or deserialize stored YAML nodes.

## report



processor
: Puppet's report processor.  Processes the report with each of
  the report types listed in the 'reports' setting.

processor
: Puppet's report processor.  Processes the report with each of
  the report types listed in the 'reports' setting.

rest
: Get server report over HTTP via REST.

rest
: Get server report over HTTP via REST.

yaml
: Store last report as a flat file, serialized using YAML.

yaml
: Store last report as a flat file, serialized using YAML.

## resource



active_record
: (undocumented)

active_record
: (undocumented)

ral
: (undocumented)

ral
: (undocumented)

rest
: (undocumented)

rest
: (undocumented)

store_configs
: (undocumented)

store_configs
: (undocumented)

## resource_type



parser
: Return the data-form of a resource type.

parser
: Return the data-form of a resource type.

rest
: Retrieve resource types via a REST HTTP interface.

rest
: Retrieve resource types via a REST HTTP interface.

## status



local
: (undocumented)

local
: (undocumented)

rest
: (undocumented)

rest
: (undocumented)



----------------

*This page autogenerated on Tue Aug 21 17:55:39 -0700 2012*
