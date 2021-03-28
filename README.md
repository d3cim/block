# block

A collection of domains, wildcards and substrings designed for [`dnscrypt-proxy`](https://github.com/DNSCrypt/dnscrypt-proxy) filter method.

- __allowed-names.txt:__ it's the file used to unblock a specific domain blocked by some substring/wildcard contained in the blocklists.
- __domains-blocklist.conf:__ it's used to configure the sources to merge during the process.
- __domains-blocklist-local-additions.txt:__ it's used during the generation process to add your own additions and remove duplicates from the sources.
- __domains-allowlist.txt:__ it's used during the generation process to remove legit domains.
- __example-blocklist.txt:__ it contains valid name patterns for this purpose.
- __generate-domains-blocklist.py:__ it's the script used to launch the generation process.

## Sources

Updated sources from the following locations are always merged and included.

#### blocked-names.txt

| Source | Maintainer(s) | Description | Home Page | RAW Source | License |
|--------|:-------------:|-------------|:---------:|:----------:|:-------:|
OISD: Domains (wildcards) [full] | sjhgvr | A merged domain list from a variety of other lists  | [LINK](https://oisd.nl/) | [RAW](https://dblw.oisd.nl/) | All Rights Reserved |
 domains-blocklist-local-additions.txt | quindecim | Domains, wildcards and substrings collection | [LINK](https://git.nixnet.services/quindecim/block) | [RAW](https://git.nixnet.services/quindecim/block/raw/branch/master/config/domains-blocklist-local-additions.txt) | GPLv3 |
 domains-allowlist.txt | quindecim | Legit domains collection | [LINK](https://codeberg.org/quindecim/block) | [RAW](https://codeberg.org/quindecim/block/raw/branch/master/config/domains-allowlist.txt) | GPLv3 |

#### blocked-ips.txt

| Source | Maintainer(s) | Description | Home Page | RAW Source | License |
|--------|:-------------:|-------------|:---------:|:----------:|:-------:|
DNSCrypt: Rebind Protection | jedisct1 | DNS rebinding protection | [LINK](https://en.wikipedia.org/wiki/DNS_rebinding) | [RAW](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Filters#dns-rebinding-protection) | ISC |

## Build

To generate your own list you can clone this repo, move into the `config` folder, edit files according to your needs and run this command:
```
python3 generate-domains-blocklist.py > list.txt.tmp && mv -f list.txt.tmp list
```