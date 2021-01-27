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
OISD | sjhgvr | A merged domain list from a variety of other lists  | [LINK](https://oisd.nl/) | [RAW](https://dbl.oisd.nl/) | None? |
The Quantum Ad-List | The_Quantum_Alpha & Co. | Blocklist of ads and tracker domains (made by an AI) | [LINK](https://gitlab.com/The_Quantum_Alpha/the-quantum-ad-list) | [RAW](https://gitlab.com/The_Quantum_Alpha/the-quantum-ad-list/-/raw/master/For%20hosts%20file/The_Quantum_Ad-List.txt) | The Unlicense |
 domains-blocklist-local-additions.txt | quindecim | Domains, wildcards and substrings collection | [LINK](https://git.nixnet.services/quindecim/block) | [RAW](https://git.nixnet.services/quindecim/block/raw/branch/master/domains-blocklist-local-additions.txt) | GPLv3 |
 domains-allowlist.txt | quindecim | Legit domains collection | [LINK](https://git.nixnet.services/quindecim/block) | [RAW](https://git.nixnet.services/quindecim/block/raw/branch/master/domains-allowlist.txt) | GPLv3 |

#### blocked-ips.txt

| Source | Maintainer(s) | Description | Home Page | RAW Source | License |
|--------|:-------------:|-------------|:---------:|:----------:|:-------:|
DNSCrypt: Rebind Protection | jedisct1 | DNS rebinding protection | [LINK](https://en.wikipedia.org/wiki/DNS_rebinding) | [RAW](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Filters#dns-rebind-protection) | ISC |
Energized: IP Extension | Energized Team | Malicious IP protection | [LINK](https://energized.pro/) | [RAW](https://block.energized.pro/extensions/ips/formats/list.txt) | MIT |

## Build

To generate your own list you can clone this repo, edit files according to your needs and run this command:
```
python generate-domains-blocklist.py > list.txt.tmp && mv -f list.txt.tmp list
```

## Notice

<table>
<tr>
<td>
When it has reached a stable level the blocklist will be shared here as release.
</td>
</tr>
</table>