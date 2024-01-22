# block

Hardened blocklist project designed for [dnscrypt-proxy](https://github.com/DNSCrypt/dnscrypt-proxy) [filter method](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Filters).

## Introduction

- `allowed-names.txt` is the file used to bypass a specific domain blocked by `blocked-names.txt` file.
- `blocked-names.txt` is the file used to block domains.
- `domains-blocklist.conf` is used before the generation process to define the sources to merge.
- `domains-blocklist-local-additions.txt` is used before the generation process to merge your inclusions.
- `domains-allowlist.txt` is used before the generation process to merge your exclusions.
- `generate-domains-blocklist.py` is the script used during the build process.

## Sources

### allowed-names.txt

| Source | Maintainer(s) | Description | Home Page | RAW Source | License |
|--------|:-------------:|-------------|:---------:|:----------:|:-------:|

### blocked-ips.txt

| Source | Maintainer(s) | Description | Home Page | RAW Source | License |
|--------|:-------------:|-------------|:---------:|:----------:|:-------:|
DNSCrypt: Rebind Protection | jedisct1 | DNS rebinding protection | [LINK](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Filters#dns-rebinding-protection) | - | [ISC](https://github.com/DNSCrypt/dnscrypt-proxy/blob/master/LICENSE) |

### blocked-names.txt

#### Inclusions

| Source | Maintainer(s) | Description | Home Page | RAW Source | License |
|--------|:-------------:|-------------|:---------:|:----------:|:-------:|
Developer Dan: AMP Hosts | Daniel (lightswitch05) | Block Google's Accelerated Mobile Pages (AMP). | [LINK](https://github.com/lightswitch05/hosts) | [RAW](https://www.github.developerdan.com/hosts/lists/amp-hosts-extended.txt) | [Apache-2.0](https://github.com/lightswitch05/hosts/blob/master/LICENSE) |
domains-blocklist-local-additions.txt | d3cim | Domains, wildcards and substrings collection. | [LINK](https://github.com/d3cim) | [RAW](https://raw.githubusercontent.com/d3cim/block/master/config/domains-blocklist-local-additions.txt) | [GPLv3](https://github.com/d3cim/block/blob/master/LICENSE.md) |
hagezi: DoH Bypass | hagezi (Gerd) | A merged list from a variety of other lists. | [LINK](https://github.com/hagezi/dns-blocklists) | [RAW](https://raw.githubusercontent.com/hagezi/dns-blocklists/main/wildcard/doh-onlydomains.txt) | [GPLv3](https://github.com/hagezi/dns-blocklists/blob/main/LICENSE) |
hagezi: Threat Intelligence Feeds | hagezi (Gerd) | A merged list from a variety of other lists. | [LINK](https://github.com/hagezi/dns-blocklists) | [RAW](https://raw.githubusercontent.com/hagezi/dns-blocklists/main/wildcard/tif-onlydomains.txt) | [GPLv3](https://github.com/hagezi/dns-blocklists/blob/main/LICENSE) |
hagezi: Ultimate | hagezi (Gerd) | A merged list from a variety of other lists. | [LINK](https://github.com/hagezi/dns-blocklists) | [RAW](https://raw.githubusercontent.com/hagezi/dns-blocklists/main/wildcard/ultimate-onlydomains.txt) | [GPLv3](https://github.com/hagezi/dns-blocklists/blob/main/LICENSE) |
OISD: big | Stephan (sjhgvr) | A merged list from a variety of other lists. | [LINK](https://oisd.nl/) | [RAW](https://big.oisd.nl/domainswild) | All Rights Reserved |

#### Exclusions

| Source | Maintainer(s) | Description | Home Page | RAW Source | License |
|--------|:-------------:|-------------|:---------:|:----------:|:-------:|
domains-allowlist.txt | d3cim | Legit domains collection. | [LINK](https://github.com/d3cim) | [RAW](https://raw.githubusercontent.com/d3cim/block/master/config/domains-allowlist.txt) | [GPLv3](https://github.com/d3cim/block/blob/master/LICENSE.md) |

## Build

To generate your own list you can clone this repo, move into the `config` folder, edit files according to your needs and run this command:

#### Linux
```
python3 generate-domains-blocklist.py > list.txt.tmp && mv -f list.txt.tmp list
```
#### Windows
```
py generate-domains-blocklist.py > list.txt
```

