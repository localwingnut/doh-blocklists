# DoH blocklists

Public DNS-over-HTTPS resolver lists for firewall blocking (pfBlockerNG).

- `domains.txt`: DoH resolver hostnames (for DNS blocking).
- `ipv4-deny.txt`, `ipv6-deny.txt`: DoH resolver addresses (for firewall rules).

Built by running dibdot/DoH-IP-blocklists `doh-lookup.sh` locally (unmodified except resolver routing and parallelism). Nothing was excluded, so the IPv4 list includes plain DNS resolvers (1.1.1.1, 8.8.8.8, 9.9.9.9, and others) and addresses inside shared Cloudflare ranges. Blocking those IPs will break ordinary DNS or unrelated sites. Review before using as a deny list.

Snapshot built 2026-10-22 (refreshed run). Resolver addresses change, so rebuild before long-term use.
