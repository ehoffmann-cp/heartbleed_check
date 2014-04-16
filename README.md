#CloudPassage Heartbleed Check Example

Version: *1.0*
<br />
Author: *Eric Hoffmann* - *ehoffmann@cloudpassage.com*

Users can use the provided example script to check for the presence of CVE-2014-0160 aka Heartbleed. It uses the Halo API to get the details of the last scheduled or manually launched SVA scan for all active servers. It then checks for the OpenSSL package and if CVE-2014-0160 is in the list of identified CVEs.

##Requirements and Dependencies

To run, these scripts require

* Ruby installed on the host that runs the scripts.
* Ruby gems: oauth2, rest-client, json
* A read-only Halo API key/secret (for GETs); copy them from the Halo Portal

##List of Files

* **check_for_cve-2014-0160.rb**  - Ruby script which leverages the Halo API to check for the presence of CVE-2014-0160 
* **README.md**  -  This ReadMe file
* **LICENSE.txt**  -  License from CloudPassage

##Usage

1. Copy the two-part Halo API key from the Halo Portal into the proper location in the scripts.
2. Execute the script.

```ruby check_for_cve-2014-0160.rb
ip-10-123-254-12, 53.215.74.1, centos,6.3, openssl.x86_64, 1.0.0-25.el6_3.1, notvuln
ip-10-10-254-13, 54.192.200.254, ubuntu,12.04, openssl, 1.0.1-4ubuntu5.11, CVE-2014-0160
Checked 2 servers total for OpenSSL and CVE-2014-0160
```
