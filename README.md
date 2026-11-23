# LotusCom Janus+ Lab Release, 10 users

LotusCom Janus is a cloud-native packet core for mobile operators, private 5G,
and MEC: 4G EPC and 5G Core in one integrated system, built on 3GPP Release 18,
under one licence.

LotusCom Janus carries data. LotusCom Janus+ is Janus with IMS added, so it
also carries voice: VoNR over 5G, VoLTE over 4G, and WiFi Calling over WiFi,
with SIP and RTP media. This package is the Janus+ lab build.

This build is 3GPP R-18-based and includes Dual Core, the 5GC and 4G EPC,
network slicing, policy control, WiFi offload through N3IWF and ePDG, IMS
voice with SIP and RTP, and a NOC console.

The build contains AMF, SMF, UPF, AUSF, UDM, UDR, NRF, PCF, NSSF, and NEF for
5G; MME, SGW, PGW, and HSS for 4G; N3IWF and ePDG for WiFi offload; P-CSCF,
I-CSCF, S-CSCF, and MRF for IMS; and the NOC console.

Locked, closed build of Janus+ for lab testing and evaluation, 23 November
2026. This release is limited to 10 registered subscribers, 2 eNB and 2 gNB,
and expires on 23 November 2027. Janus+ is a product of Lotus Communication
Systems Inc.

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
