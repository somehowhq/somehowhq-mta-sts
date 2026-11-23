# somehowhq.com MTA-STS policy

Serves `https://mta-sts.somehowhq.com/.well-known/mta-sts.txt` with GitHub Pages: the MTA-STS policy for mail to `somehowhq.com` (RFC 8461). It tells sending servers to deliver only over TLS to `smtp.google.com`.

- **Mode:** `testing`. Failures are reported to the TLS-RPT address in `_smtp._tls.somehowhq.com` and mail is still delivered. Switch to `enforce` once the reports are clean, then bump the `id` in the `_mta-sts.somehowhq.com` TXT record.
- **DNS:** `mta-sts.somehowhq.com` is a DNS-only CNAME to `somehowhq.github.io` (the repo moved into the somehowhq org on 2026-11-24). Both records are made by turian/superadmin `cloudflare-dns-records` requests.
- **Punch list:** https://github.com/somehowhq/governance/issues/2.
- **Move it** to the `somehowhq` GitHub org once that org exists.
