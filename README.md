# CipherDNS.co.za
A self-managed DNS resolver publically available for use based in South Africa.

# Public Hyperlocal Secure DNS Resolver (South Africa)

A high-performance, privacy-focused public DNS resolver architecture designed for low-latency, cryptographically secure name resolution within South Africa. 

Our dual-edge infrastructure pairs high-efficiency Nginx reverse-proxying for TCP-based layers with direct user-space UDP worker binding for next-generation QUIC handling, upstreamed to a hardened Unbound DNS core.

## 🔒 Security & Privacy Policy

* **Zero Logging:** Client source IP addresses are processed entirely in-memory and are never written to persistent disks or database logs.
* **DNSSEC Validation:** Full cryptographic verification of upstream root zones to prevent DNS cache poisoning and man-in-the-middle hijacking.
* **Unfiltered & Natural:** We do not implement content filtering, blocklists, or resolution modifications. You receive raw DNS responses.

## ⚙️ Connection Endpoints & DNS Stamps ( CapeTown-01 )

### 1. DNS-over-TLS (DoT)
* **Address:** `tls://ct1-doh.cipherdns.co.za:853`

### 2. DNS-over-HTTPS (DoH)
* **Address:** `https://ct1-doh.cipherdns.co.za/dns-query`
* **Stamp:** `sdns://AgcAAAAAAAAADjEwMi4yMDkuMjEuMTc2IN9Gmj6Z-sGI6kgHGCuJ-2IbQ7MV1jsrEVngkymImwm7F2N0MS1kb2guY2lwaGVyZG5zLmNvLnphCi9kbnMtcXVlcnk`

### 3. DNS-over-QUIC (DoQ)
* **Address:** `quic://ct1-doq.cipherdns.co.za:853`

### 4. DNSCrypt
* **Provider:** `2.dnscrypt-cert.ct1.cipherdns.co.za`
* **Stamp:** `sdns://AQcAAAAAAAAAEzEwMi4yMDkuMjEuMTc2Ojg0NDMgXnTgm6IgQnhUO3h_6tAlE0lQ5dXjfG2JmvSXCde6P6QjMi5kbnNjcnlwdC1jZXJ0LmN0MS5jaXBoZXJkbnMuY28uemE`

### 5. Anonymized DNS (Relay)
* **Stamp:** `sdns://gRMxMDIuMjA5LjIxLjE3Njo4NDQz`
