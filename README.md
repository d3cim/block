# block

A collection of domains, wildcards and substrings designed for [`dnscrypt-proxy`](https://github.com/DNSCrypt/dnscrypt-proxy) filter method.

- __domains-blocklist.conf:__ is used to configure the sources to merge during the process.
- __domains-blocklist-local-additions.txt:__ is used during the generation process to add your own additions and remove duplicates from the sources.
- __domains-allowlist.txt:__ is used during the generation process to remove legit domains.
- __example-blocklist.txt:__ contains valid name patterns for this purpose.
- __generate-domains-blocklist.py:__ is the script used to launch the generation process.

### Sources

Updated sources from the following locations are always merged and included.

| Source | Maintainer(s) | Description | Home Page | RAW Source | License |
|--------|:-------------:|-------------|:---------:|:----------:|:-------:|
OISD | sjhgvr | A merged domain list from a variety of other lists  | [LINK](https://oisd.nl/) | [RAW](https://dbl.oisd.nl/) | None? |
The Quantum Ad-List | The_Quantum_Alpha & Co. | Blocklist of ads and tracker domains (made by an AI) | [LINK](https://gitlab.com/The_Quantum_Alpha/the-quantum-ad-list) | [RAW](https://gitlab.com/The_Quantum_Alpha/the-quantum-ad-list/-/raw/master/For%20hosts%20file/The_Quantum_Ad-List.txt) | The Unlicense |

### Build

To generate your own list you can clone this repo, edit files according to your needs and run this command:
```
python generate-domains-blocklist.py > list.txt.tmp && mv -f list.txt.tmp list
```

### Notice

<table>
<tr>
<td>
When it has reached a stable level the blocklist will be shared here as release.
</td>
</tr>
</table>