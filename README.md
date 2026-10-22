# DoH blocklists

Public DNS-over-HTTPS resolver lists for firewall blocking (pfBlockerNG).

- `domains.txt`: DoH resolver hostnames (for DNS blocking).
- `ipv4-deny.txt`, `ipv6-deny.txt`: DoH resolver addresses (for firewall rules).

Built from the dibdot/DoH-IP-blocklists domain list. Plain DNS resolvers and shared Cloudflare ranges were removed from the IP lists. Snapshot built 2026-10-21; resolver addresses change, so rebuild before long-term use.
