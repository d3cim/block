# block

A collection of domains, wildcards and substrings designed for [`dnscrypt-proxy`](https://github.com/DNSCrypt/dnscrypt-proxy) filter method.

- __domains-blacklist-local-additions:__ is used during the generation process to remove duplicates from sources and filter the web content once the [`blacklist`](https://git.nixnet.xyz/quindecim/dnscrypt-proxy-android/src/branch/master/config/blacklist.txt) file is applied.
- __domains-whitelist:__ is used during the generation process to remove legit domains from the final [`blacklist`](https://git.nixnet.xyz/quindecim/dnscrypt-proxy-android/src/branch/master/config/blacklist.txt).
- __example-blacklist:__ contains valid name patterns for this purpose.

### Sources

Updated sources from the following locations are always merged and included.

| Source | Maintainer(s) | Description | Home Page | RAW Source | License |
|--------|:-------------:|-------------|:---------:|:----------:|:-------:|
Frogeye | Geoffrey Frogeye | Blocklist of 1st-party trackers | [LINK](https://hostfiles.frogeye.fr/) | [RAW](https://hostfiles.frogeye.fr/firstparty-trackers.txt) | All Rights Reserved |
NextDNS | NextDNS | Blocklist of 1st-party trackers | [LINK](https://nextdns.io/) | [RAW](https://raw.githubusercontent.com/nextdns/cname-cloaking-blocklist/master/domains) | MIT |
Energized Ultimate | Energized Team | A merged domains file from a variety of other lists  | [LINK](https://app.energized.pro/) | [RAW](https://block.energized.pro/ultimate/formats/domains.txt) | MIT |
Energized Regional | Energized Team | A merged domains file from a variety of other lists  | [LINK](https://app.energized.pro/) | [RAW](https://block.energized.pro/extensions/regional/formats/domains.txt) | MIT |
Energized Xtreme | Energized Team | Blocklist of ads and tracking servers  | [LINK](https://app.energized.pro/) | [RAW](https://block.energized.pro/extensions/xtreme/formats/domains.txt) | MIT |

### Notice

<table>
<tr>
<td>
When it has reached a stable level the blacklist will be shared here as release.
</td>
</tr>
</table>