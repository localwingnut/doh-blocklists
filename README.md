# DoH blocklists

Public DNS-over-HTTPS resolver lists for firewall blocking (pfBlockerNG).

- `domains.txt`: DoH resolver hostnames (DNS blocking).
- `ipv4-deny.txt`, `ipv6-deny.txt`: DoH resolver addresses, Apple addresses removed.
- `apple-ipv4.txt`: addresses in Apple's 17.0.0.0/8 (removed from the DoH IPv4 list).
- `apple-ipv6.txt`: addresses in Apple's 2620:149::/32 and 2403:300::/32 (removed from the DoH IPv6 list).

Built from dibdot/DoH-IP-blocklists `doh-lookup.sh` run locally. Nothing was excluded except the Apple split above, so the DoH lists still include plain DNS resolvers (1.1.1.1, 8.8.8.8, 9.9.9.9, and others) and addresses inside shared Cloudflare ranges. Review before using as a deny list.

Snapshot built 2026-10-22 (split version). Resolver addresses change, so rebuild before long-term use.
