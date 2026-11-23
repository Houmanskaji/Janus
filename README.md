# LotusCom Janus+ Lab Release, 10 users

Locked, closed build of Janus+ for lab testing and evaluation, 23 November 2026.

Janus+ is Janus plus IMS: one integrated core, 5GC plus 4G EPC plus IMS,
with SIP and RTP, under one licence. This release is limited to
10 registered subscribers, 2 eNB and 2 gNB, and expires on 23 November 2027.
Janus+ is a product of Lotus Communication Systems Inc.

## What is in this package

- `janus`: the Janus+ binary, Linux 64 bit. No source code is included.
- `licence-tool`: checks a licence file and shows its limits.
- `janus.licence`: the signed 10 user licence for this release.
- `janus.json`: configuration: node name, licence key, service addresses.
- `JanusPlus-Lab-Installation-and-Setup-Guide-EN.docx`: installation and setup guide.
- `SHA256SUMS.txt`: checksums. Run `sha256sum -c SHA256SUMS.txt` before you run anything.

## Quick start

```
chmod +x janus licence-tool
./janus -config janus.json
curl http://127.0.0.1:8080/status
```

Read the guide for provisioning subscribers and for the first voice test.
The NOC console is at http://127.0.0.1:8080.

## Licence

The binary refuses to start without a valid licence. The eleventh
subscriber is refused with HTTP 403. A new licence, with a different
limit or a longer validity, is issued by LotusCom only:
houman@lotuscom.net.

The private key that signs licences never leaves LotusCom and is not
in this package. Do not ask for it.
