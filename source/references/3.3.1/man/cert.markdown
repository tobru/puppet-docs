---
layout: default
nav: /_includes/references_man.html
title: puppet cert Man Page
---

<div class='mp'>
<h2 id="NAME">NAME</h2>
<p class="man-name">
  <code>puppet-cert</code> - <span class="man-whatis">Manage certificates and requests</span>
</p>

<h2 id="SYNOPSIS">SYNOPSIS</h2>

<p>Standalone certificate authority. Capable of generating certificates,
but mostly used for signing certificate requests from puppet clients.</p>

<h2 id="USAGE">USAGE</h2>

<p>puppet cert <var>action</var> [-h|--help] [-V|--version] [-d|--debug] [-v|--verbose]
  [--digest <var>digest</var>] [<var>host</var>]</p>

<h2 id="DESCRIPTION">DESCRIPTION</h2>

<p>Because the puppet master service defaults to not signing client
certificate requests, this script is available for signing outstanding
requests. It can be used to list outstanding requests and then either
sign them individually or sign all of them.</p>

<h2 id="ACTIONS">ACTIONS</h2>

<p>Every action except 'list' and 'generate' requires a hostname to act on,
unless the '--all' option is set.</p>

<dl>
<dt class="flush">clean</dt><dd><p>Revoke a host's certificate (if applicable) and remove all files
related to that host from puppet cert's storage. This is useful when
rebuilding hosts, since new certificate signing requests will only be
honored if puppet cert does not have a copy of a signed certificate
for that host. If '--all' is specified then all host certificates,
both signed and unsigned, will be removed.</p></dd>
<dt>fingerprint</dt><dd><p>Print the DIGEST (defaults to the signing algorithm) fingerprint of a
host's certificate.</p></dd>
<dt>generate</dt><dd><p>Generate a certificate for a named client. A certificate/keypair will
be generated for each client named on the command line.</p></dd>
<dt class="flush">list</dt><dd><p>List outstanding certificate requests. If '--all' is specified, signed
certificates are also listed, prefixed by '+', and revoked or invalid
certificates are prefixed by '-' (the verification outcome is printed
in parenthesis).</p></dd>
<dt class="flush">print</dt><dd><p>Print the full-text version of a host's certificate.</p></dd>
<dt class="flush">revoke</dt><dd><p>Revoke the certificate of a client. The certificate can be specified either
by its serial number (given as a hexadecimal number prefixed by '0x') or by its
hostname. The certificate is revoked by adding it to the Certificate Revocation
List given by the 'cacrl' configuration option. Note that the puppet master
needs to be restarted after revoking certificates.</p></dd>
<dt class="flush">sign</dt><dd><p>Sign an outstanding certificate request.</p></dd>
<dt class="flush">verify</dt><dd><p>Verify the named certificate against the local CA certificate.</p></dd>
</dl>


<h2 id="OPTIONS">OPTIONS</h2>

<p>Note that any configuration parameter that's valid in the configuration
file is also a valid long argument. For example, 'ssldir' is a valid
configuration parameter, so you can specify '--ssldir <var>directory</var>' as an
argument.</p>

<p>See the configuration file documentation at
http://docs.puppetlabs.com/references/stable/configuration.html for the
full list of acceptable parameters. A commented list of all
configuration options can also be generated by running puppet cert with
'--genconfig'.</p>

<dl>
<dt class="flush">--all</dt><dd><p>Operate on all items. Currently only makes sense with the 'sign',
'clean', 'list', and 'fingerprint' actions.</p></dd>
<dt>--digest</dt><dd><p>Set the digest for fingerprinting (defaults to the the digest used when
signing the cert). Valid values depends on your openssl and openssl ruby
extension version.</p></dd>
<dt class="flush">--debug</dt><dd><p>Enable full debugging.</p></dd>
<dt class="flush">--help</dt><dd><p>Print this help message</p></dd>
<dt>--verbose</dt><dd><p>Enable verbosity.</p></dd>
<dt>--version</dt><dd><p>Print the puppet version number and exit.</p></dd>
</dl>


<h2 id="EXAMPLE">EXAMPLE</h2>

<pre><code>$ puppet cert list
culain.madstop.com
$ puppet cert sign culain.madstop.com
</code></pre>

<h2 id="AUTHOR">AUTHOR</h2>

<p>Luke Kanies</p>

<h2 id="COPYRIGHT">COPYRIGHT</h2>

<p>Copyright (c) 2011 Puppet Labs, LLC Licensed under the Apache 2.0 License</p>

</div>
