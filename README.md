# block

A collection of domains, wildcards and substrings designed for [`dnscrypt-proxy`](https://github.com/DNSCrypt/dnscrypt-proxy) filter method.

- __domains-blocklist.conf:__ is used to configure the sources to merge during the process.
- __domains-blocklist-local-additions:__ is used during the generation process to add your own additions and remove duplicates from the sources.
- __domains-allowlist:__ is used during the generation process to remove legit domains.
- __example-blocklist:__ contains valid name patterns for this purpose.
- __generate-domains-blocklist.py:__ is the script used to launch the generation process.

### Sources

Updated sources from the following locations are always merged and included.

| Source | Maintainer(s) | Description | Home Page | RAW Source | License |
|--------|:-------------:|-------------|:---------:|:----------:|:-------:|
Energized Ultimate | Energized Team | A merged domains file from a variety of other lists  | [LINK](https://app.energized.pro/) | [RAW](https://block.energized.pro/ultimate/formats/domains.txt) | MIT |
Energized Regional | Energized Team | A merged domains file from a variety of other lists  | [LINK](https://app.energized.pro/) | [RAW](https://block.energized.pro/extensions/regional/formats/domains.txt) | MIT |
Energized Xtreme | Energized Team | Blocklist of ads and tracking servers  | [LINK](https://app.energized.pro/) | [RAW](https://block.energized.pro/extensions/xtreme/formats/domains.txt) | MIT |
Frogeye 1st-party Trackers | Geoffrey Frogeye | Blocklist of 1st-party trackers | [LINK](https://hostfiles.frogeye.fr/) | [RAW](https://hostfiles.frogeye.fr/firstparty-trackers.txt) | All Rights Reserved |
NextDNS 1st-party Trackers | NextDNS | Blocklist of 1st-party trackers | [LINK](https://nextdns.io/) | [RAW](https://raw.githubusercontent.com/nextdns/cname-cloaking-blocklist/master/domains) | MIT |

### Notice

<table>
<tr>
<td>
When it has reached a stable level the blocklist will be shared here as release.
</td>
</tr>
</table>