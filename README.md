# DoH blocklists

Public DNS-over-HTTPS resolver lists for firewall blocking (pfBlockerNG). Apple's own services are split into separate files so they can be handled on their own.

| File | Contents |
|---|---|
| `domains.txt` | DoH resolver hostnames (Apple's own names removed) |
| `ipv4-deny.txt` | DoH resolver IPv4 addresses (Apple's 17.0.0.0/8 removed) |
| `ipv6-deny.txt` | DoH resolver IPv6 addresses (Apple's IPv6 ranges removed) |
| `apple.domains.txt` | Apple's DNS-over-HTTPS and iCloud Private Relay hostnames |
| `ipv4-apple-deny.txt` | Addresses in Apple's 17.0.0.0/8 |
| `ipv6-apple-deny.txt` | Addresses in Apple's 2620:149::/32 and 2403:300::/32 |

Built from dibdot/DoH-IP-blocklists `doh-lookup.sh`, run locally. Nothing was excluded except the Apple split, so the DoH lists still include plain DNS resolvers (1.1.1.1, 8.8.8.8, 9.9.9.9, and others) and addresses inside shared Cloudflare ranges. Review before using as a deny list.

Snapshot built 2026-10-22. Resolver addresses change, so rebuild before long-term use.
